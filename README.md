# 概要
ViewTypeで表示するセルを分けるRecyclerViewの最小限の構成  

# 詳細
SectionGroup: それぞれのSectionを管理する  
HeaderSection: ヘッダーを持つSection  
NoHeaderSection: ヘッダーを持たないSection  

# 手順

## Section
1. interface Section を追加  
2. class SectionGroup を追加  
3. class NoHeaderSection を追加  
4. class SectionHeaderModel を追加  
5. class HeaderSection を追加  

## Adapter
1. Adapterクラスの引数からリストを削除  
2. Adapterクラスの引数にSectionGroupを追加
3. ovarride fun onBindViewHolderのlist[position] をsectionGroup.itemAt(position)に変更  
4. ovarride fun getItemViewTypeのlist[position] をsectionGroup.itemAt(position)に変更  
5. override fun getItemCount のreturn をsectionGroup.totalCount() に変更  
6. inner class SectionHeaderHolder を追加
7. onCrateViewHolder にSectionHeaderのViewHolderを追加
8. onBindViewHolder にSectionHeaderを追加  

## Activity
1. プロパティにsectionGroupを追加
2. adapterのインスタンス化する際にsectionGropを渡す
3. sectionGroup にappendする

## layout
1. SectionHeaderのレイアウトを作る



