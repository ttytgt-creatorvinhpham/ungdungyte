# 🔐 Gemini AI Proxy cho MedCareLink

Đây là server proxy giúp gọi Gemini API từ tiện ích Chrome AI mà không lộ API Key.

## 🧠 Endpoint AI:

## 🔧 Biến môi trường (Environment Variable – cấu hình trong Vercel)

- `GEMINI_API_KEY`: Dán key lấy từ [https://makersuite.google.com/app/apikey](https://makersuite.google.com/app/apikey)

## 📦 Dùng với tiện ích Chrome như sau:

```js
fetch('https://ai.ungdungyte.io.vn/api/proxy', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify({
    prompt: 'Bệnh nhân mạch 90, huyết áp 120/80, sốt nhẹ 38 độ. Hãy chẩn đoán sơ bộ và đề xuất cận lâm sàng.'
  })
})
.then(res => res.json())
.then(data => console.log(data.reply));
