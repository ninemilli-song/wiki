# 2021年1月 cc借调支持

## 修改缺陷

分支：@songxg/cc-support

账号：17778131921  wqw36641  
https://test-cloud.chanjet.com/cc/ulqg9nhssek8/g8jk7thy46/index.html#/

---

1. https://jira2.rd.chanjet.com/browse/CC-4857 (done 2020/12/24)

    与 4 重复

---

2. https://jira2.rd.chanjet.com/browse/HSYN-20525 (未重现)

---

3. https://jira2.rd.chanjet.com/browse/CC-4989

---

4. https://jira2.rd.chanjet.com/browse/HSYN-25988 (done 2020/12/24)

文件：ExpenseAllocationView.tsx
方法：renderTotalPart
变量：amountAllocatableTotal

---

5. https://jira2.rd.chanjet.com/browse/CC-5055 (done 2020/12/23)

单据日期不可编辑：

组件：
voucherDateNo

根据prsenter中的 voucherDateCanEdit 控制是否可编辑

解决：

presenter中计算 voucherDateCanEdit 需要添加单据的是否已核销

http://localhost:8080/hsy/uyeam0pzme02/s7pixe64u3/index.html#/voucher-goods-issue-perfect/edit1283105748156416?activePrompt=true&closePrompt=true&closeable=true&leavePrompt=true&lock=false&pageId=voucher-goods-issue-perfect%2Fedit1283105748156416&pageParams=%7B%22action%22%3A%22edit%22%2C%22voucherId%22%3A1283105748156416%2C%22copyId%22%3A0%2C%22scopeList%22%3A%5B%5D%2C%22activeFromTab%22%3Afalse%2C%22isChange%22%3Atrue%7D&path=voucher-goods-issue-perfect%2F%3Ats&tabId=voucher-goods-issue-perfect&tabLabel=%E9%94%80%E8%B4%A7%E5%8D%95&_k=m7odaf

---

6. https://jira2.rd.chanjet.com/browse/HSYN-27059 (done 2021/1/4)

node端商品查询gql需要添加这两个字段
productId.productFeatureTypeAppl
productId.isMultiSpecEnabled

---

7. https://jira2.rd.chanjet.com/browse/HSYN-20639 (done)
8. https://jira.rd.chanjet.com/browse/HSYYF-2637
工程：cc-front-pub/cc-front-biz-app-service
修改文件：getMobileBizDateChangeHandler.ts / getMobileBizDateChangedHandler

```
//现在加上促销会改变总金额,所以需要算一下总金额等
-    processBlock.add(getSalesVoucherSummaryTotalCalcBlock(ctx));
+    processBlock.add(getMobileSalesVoucherSummaryTotalCalcBlock(ctx));
```

