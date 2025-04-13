# React - [react.dev](https://react.dev/)
- React, kullanıcı arayüzleri oluşturmak için kullanılan bir JavaScript kütüphanesidir.
- Her şey "component" (bileşen) yapısı etrafında şekillenir.
- Önce bir yapı kurulur, ardından sadece veri aktarımı yapılır.
- Componentler, kullanıcı arayüzlerinin bağımsız parçalarıdır.

## Node.js - [nodejs.org](https://nodejs.org/tr) 
- Node.js, JavaScript'in sunucu tarafında çalışmasını sağlayan bir çalışma ortamıdır.
- Resmi sitesinden LTS (Long Term Support) sürümünü indirilmelidir.
- Sürüm kontrolü sağlamak üzere komut satırına yazmamız gereken kod:

```bash
node --version
```
## # first-app
###  * Proje Oluşturma
VSCode > Terminal > New Terminal
```bash
npx create-react-app project-name
cd project-name
npm start
```
### * Proje Yapısı
📁 public/
- Statik varlıkları barındırır.
- Tarayıcıya sunulur.
public > index.html
```html
<div id="root"></div>
```
JavaScript ile dinamik olarak içerik eklenecek olan ana kapsayıcı (container) elemandır. Uygulama bu elementin içinde yaşar.

📁 node_modules/

Projedeki tüm kurulu paketlerin yer aldığı klasördür.

📁 src/

Tüm React bileşenlerinin, stillerinin ve mantığının bulunduğu ana klasör.

📁 components/

Kendi oluşturduğumuz küçük bileşenleri (component) koyduğumuz yerdir.

📄 package.json
Projeye ait tüm bilgileri içerir:

Proje adı, versiyon, bağımlılıklar, script'ler vs.

###  * Greeting.jsx
src > components (New Folder) > Greeting.jsx (New File)
```javascript
//Greeting.jsx
import React from 'react'

const Greeting = () => {
  return (
    <div>My First Component</div>
  )
}

export default Greeting;
```
src > App.js
```javascript
function App() {
  return (
    <div className="App">
      <Greeting/>
    </div>
  );
}
```