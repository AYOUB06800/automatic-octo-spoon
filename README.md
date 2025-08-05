plaintext
📦 src/
├── App.js               ← الصفحة الرئيسية
├── components/
│   └── ProductCard.js   ← مكون عرض المنتج
├── data/
│   └── products.js      ← بيانات المنتجات
    products.js
        js
        const products = [
  {
    id: 1,
    name: "ساعة ذكية",
    price: "299 درهم",
    image: "https://via.placeholder.com/150",
  },
  {
    id: 2,
    name: "سماعات بلوتوث",
    price: "149 درهم",
    image: "https://via.placeholder.com/150",
  },
  {
    id: 3,
    name: "حقيبة ظهر",
    price: "199 درهم",
    image: "https://via.placeholder.com/150",
  },
];

export default products;
ProductCard.js
jsx
import React from "react";

const ProductCard = ({ product }) => (
  <div className="bg-white rounded-lg shadow p-4 text-center">
    <img src={product.image} alt={product.name} className="mx-auto mb-2 w-32 h-32 object-cover" />
    <h2 className="text-lg font-semibold">{product.name}</h2>
    <p className="text-green-600 font-bold">{product.price}</p>
    <button className="mt-2 bg-blue-500 text-white px-4 py-1 rounded hover:bg-blue-600">
      أضف إلى السلة
    </button>
  </div>
);

export default ProductCard;
App.jsx
import React from "react";
import ProductCard from "./components/ProductCard";
import products from "./data/products";

function App() {
  return (
    <div className="min-h-screen bg-gray-100 p-4">
      <h1 className="text-2xl font-bold text-center mb-6">🛒 سوق Click</h1>
      <div className="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-4">
        {products.map((product) => (
          <ProductCard key={product.id} product={product} />
        ))}
      </div>
    </div>
  );
}

export default App;
// BottomNav.js
import React from 'react';
import BottomNav from './components/BottomNav';

function App() {
  return (
    <div className="pb-16"> {/* مساحة تحتية لتجنب تغطية المحتوى */}
      {/* باقي المحتوى */}
      <BottomNav />
    </div>
  );
}

export default function BottomNav() {
  return (
    <div className="fixed bottom-0 left-0 w-full bg-white border-t shadow-md flex justify-around py-2 text-sm sm:text-base z-50">
      <a href="#" className="flex flex-col items-center text-gray-600 hover:text-blue-500">
        <span>🏠</span>
        <span>الرئيسية</span>
      </a>
      <a href="#" className="flex flex-col items-center text-gray-600 hover:text-blue-500">
        <span>🛒</span>
        <span>السلة</span>
      </a>
      <a href="#" className="flex flex-col items-center text-gray-600 hover:text-blue-500">
        <span>🔍</span>
        <span>بحث</span>
      </a>
    </div>
  );
}Combine code snippets in Java

public class Main {
    public static void main(String[] args) {
        // Code from App.js
        System.out.println("This is the main application file");

        // Code from ProductCard.js
        System.out.println("This is the product card component");

        // Code from BottomNav.js
        System.out.println("This is the bottom navigation component");
    }
}
