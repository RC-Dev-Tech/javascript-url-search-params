# ![](https://drive.google.com/uc?id=10INx5_pkhMcYRdx_OO4rXNXxcsvPtBYq) URL參數搜尋 (URLSearchParams)
> ##### 理論請自行找，網路上有很多相關的文章，這邊只關注於範例實作的部分.

---

<!--ts-->
## 目錄:
* [簡介](#簡介)
* [實作範例](#實作範例)
<!--te-->

---

## 簡介:
當在進行網頁相關的實作，往往會碰到需要去解析URL的參數，<br>
這邊直接使用 JavaScript 的 window.location.search 屬性來獲取當前 URL 中的查詢參數。<br>
window.location.search 返回的是 URL 中 ? 符號之後的查詢字符串，包括 ? 符號本身。<br>

例如，如果當前 URL 是 '''https://example.com/page?param1=value1&param2=value2'''<br>
則 window.location.search 的值將是 '''?param1=value1&param2=value2'''<br>

要進一步處理這個查詢字符串，您可以使用 JavaScript 內建的 URLSearchParams 物件或自行解析字符串的方式來獲取特定的參數值。<br>
> 注意，這些方法只能在 Web 平台上運行，而不適用於原生平台。<br>
> 如果您需要在原生平台上處理 URL 查詢參數，則需要使用相應的原生 API 進行操作。<br>

---

## 實作範例:
```javascript
  const urlParams = new URLSearchParams(window.location.search);
  const param1 = urlParams.get('param1'); // 獲取名為 'param1' 的參數值
  const param2 = urlParams.get('param2'); // 獲取名為 'param2' 的參數值
```

---
<!--ts-->
#### [目錄 ↩](#目錄)
<!--te-->
---
