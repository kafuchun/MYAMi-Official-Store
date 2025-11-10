import Header from "./components/Header";
import { Tag, Zap, Shield, TrendingUp, Star } from "lucide-react";

export default function HomePage() {
  return (
    <div className="min-h-screen bg-gray-50 dark:bg-[#0a0a0a]">
      <Header />

      {/* Store Stats Banner */}
      <div className="bg-white dark:bg-[#1a1a1a] border-b border-gray-200 dark:border-gray-800">
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4">
          <div className="flex flex-wrap items-center justify-between gap-4">
            <div className="flex items-center gap-2">
              <div className="text-2xl font-bold text-gray-900 dark:text-white">
                MYAMi Official Store
              </div>
              <div className="bg-[#ff6a00] text-white text-xs px-2 py-1 rounded">
                Verified
              </div>
            </div>
            <div className="flex flex-wrap items-center gap-6 text-sm">
              <div className="flex items-center gap-1">
                <Star size={16} className="text-yellow-500 fill-yellow-500" />
                <span className="font-semibold">4.8</span>
                <span className="text-gray-500 dark:text-gray-400">
                  (2.5K+ Reviews)
                </span>
              </div>
              <div className="text-gray-700 dark:text-gray-300">
                <span className="font-semibold">15K+</span> Followers
              </div>
              <div className="text-gray-700 dark:text-gray-300">
                <span className="font-semibold">98.5%</span> Positive Feedback
              </div>
            </div>
          </div>
        </div>
      </div>

      {/* Coupons Section */}
      <section className="bg-gradient-to-r from-orange-50 to-red-50 dark:from-orange-900/20 dark:to-red-900/20 py-6">
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <div className="flex items-center gap-2 mb-4">
            <Tag className="text-[#ff6a00]" size={24} />
            <h2 className="text-xl font-bold text-gray-900 dark:text-white">
              Store Coupons
            </h2>
          </div>
          <div className="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-4">
            {[
              { discount: "$10 OFF", min: "$100", code: "NEW10" },
              { discount: "$25 OFF", min: "$250", code: "SOLAR25" },
              { discount: "$50 OFF", min: "$500", code: "POWER50" },
              { discount: "15% OFF", min: "$300", code: "MEGA15" },
            ].map((coupon, index) => (
              <div
                key={index}
                className="bg-white dark:bg-[#1a1a1a] rounded-lg p-4 border-2 border-dashed border-[#ff6a00] hover:shadow-lg transition-shadow"
              >
                <div className="text-2xl font-bold text-[#ff6a00]">
                  {coupon.discount}
                </div>
                <div className="text-sm text-gray-600 dark:text-gray-400 mt-1">
                  Min. spend {coupon.min}
                </div>
                <div className="flex items-center justify-between mt-3">
                  <code className="text-xs bg-gray-100 dark:bg-gray-800 px-2 py-1 rounded">
                    {coupon.code}
                  </code>
                  <button className="text-xs font-medium text-[#ff6a00] hover:underline">
                    Collect
                  </button>
                </div>
              </div>
            ))}
          </div>
        </div>
      </section>

      {/* Hero Section */}
      <section className="bg-white dark:bg-[#1a1a1a] py-12">
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <div className="flex flex-col lg:flex-row items-center gap-8">
            {/* Left Content */}
            <div className="flex-1 space-y-6">
              <div>
                <div className="inline-block bg-[#ff6a00] text-white text-sm px-3 py-1 rounded-full mb-4">
                  🔥 Hot Sale
                </div>
                <h1 className="text-4xl md:text-5xl font-bold text-gray-900 dark:text-white leading-tight">
                  Professional Solar
                  <span className="block text-[#ff6a00]">MPPT Controllers</span>
                </h1>
                <p className="text-lg text-gray-600 dark:text-gray-400 mt-4">
                  High-efficiency solar charge controllers with advanced MPPT
                  technology. Perfect for off-grid systems, RVs, boats, and home
                  solar installations.
                </p>
              </div>

              <div className="grid grid-cols-2 gap-4">
                {[
                  { icon: Zap, label: "85% Efficiency" },
                  { icon: Shield, label: "1-Year Warranty" },
                  { icon: TrendingUp, label: "30% More Power" },
                  { icon: Star, label: "CE Certified" },
                ].map((feature, index) => {
                  const Icon = feature.icon;
                  return (
                    <div key={index} className="flex items-center gap-2">
                      <div className="bg-orange-100 dark:bg-orange-900/30 p-2 rounded">
                        <Icon size={20} className="text-[#ff6a00]" />
                      </div>
                      <span className="text-sm font-medium text-gray-700 dark:text-gray-300">
                        {feature.label}
                      </span>
                    </div>
                  );
                })}
              </div>

              <div className="flex flex-wrap gap-4">
                <button className="bg-[#ff6a00] hover:bg-[#e55d00] text-white px-8 py-3 rounded-lg font-medium transition-all">
                  Shop MPPT Controllers
                </button>
                <button className="border-2 border-gray-300 hover:border-[#ff6a00] text-gray-700 hover:text-[#ff6a00] dark:border-gray-700 dark:text-gray-300 dark:hover:border-[#ff6a00] dark:hover:text-[#ff6a00] px-8 py-3 rounded-lg font-medium transition-all">
                  View All Products
                </button>
              </div>
            </div>

            {/* Right Image */}
            <div className="flex-1">
              <div className="relative bg-gradient-to-br from-orange-100 to-red-100 dark:from-orange-900/20 dark:to-red-900/20 rounded-2xl p-8">
                <img
                  src="https://images.unsplash.com/photo-1509391366360-2e959784a276?w=600&h=400&fit=crop"
                  alt="Solar Panel Installation"
                  className="w-full h-[400px] object-cover rounded-lg shadow-xl"
                />
                <div className="absolute -bottom-4 -left-4 bg-white dark:bg-[#1a1a1a] rounded-lg p-4 shadow-lg">
                  <div className="text-sm text-gray-600 dark:text-gray-400">
                    Starting at
                  </div>
                  <div className="text-2xl font-bold text-[#ff6a00]">
                    $89.99
                  </div>
                  <div className="text-xs text-gray-500 dark:text-gray-500 line-through">
                    $129.99
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      {/* Hot Deals Section */}
      <section className="py-12 bg-gray-50 dark:bg-[#0a0a0a]">
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <div className="flex items-center justify-between mb-8">
            <h2 className="text-3xl font-bold text-gray-900 dark:text-white">
              🔥 Hot Deals
            </h2>
            <a href="#" className="text-[#ff6a00] hover:underline font-medium">
              View All →
            </a>
          </div>

          <div className="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
            {[
              {
                name: "60A MPPT Solar Controller",
                price: "$89.99",
                oldPrice: "$129.99",
                image:
                  "https://images.unsplash.com/photo-1473341304170-971dccb5ac1e?w=300&h=300&fit=crop",
                rating: 4.9,
                sold: "1.2K+",
              },
              {
                name: "3000W Pure Sine Wave Inverter",
                price: "$299.99",
                oldPrice: "$399.99",
                image:
                  "https://images.unsplash.com/photo-1621905251189-08b45d6a269e?w=300&h=300&fit=crop",
                rating: 4.8,
                sold: "856",
              },
              {
                name: "DC Power Supply 0-30V 10A",
                price: "$79.99",
                oldPrice: "$109.99",
                image:
                  "https://images.unsplash.com/photo-1581092160562-40aa08e78837?w=300&h=300&fit=crop",
                rating: 4.7,
                sold: "645",
              },
              {
                name: "100A MPPT Controller LCD Display",
                price: "$149.99",
                oldPrice: "$219.99",
                image:
                  "https://images.unsplash.com/photo-1559827260-dc66d52bef19?w=300&h=300&fit=crop",
                rating: 4.9,
                sold: "2.1K+",
              },
            ].map((product, index) => (
              <div
                key={index}
                className="bg-white dark:bg-[#1a1a1a] rounded-lg overflow-hidden hover:shadow-xl transition-shadow group"
              >
                <div className="relative overflow-hidden">
                  <img
                    src={product.image}
                    alt={product.name}
                    className="w-full h-[240px] object-cover group-hover:scale-110 transition-transform duration-300"
                  />
                  <div className="absolute top-2 right-2 bg-red-500 text-white text-xs px-2 py-1 rounded">
                    SALE
                  </div>
                </div>
                <div className="p-4">
                  <h3 className="text-sm font-medium text-gray-900 dark:text-white mb-2 line-clamp-2">
                    {product.name}
                  </h3>
                  <div className="flex items-center gap-1 mb-2">
                    <Star
                      size={14}
                      className="text-yellow-500 fill-yellow-500"
                    />
                    <span className="text-sm font-medium">
                      {product.rating}
                    </span>
                    <span className="text-xs text-gray-500 dark:text-gray-400">
                      ({product.sold} sold)
                    </span>
                  </div>
                  <div className="flex items-baseline gap-2">
                    <span className="text-xl font-bold text-[#ff6a00]">
                      {product.price}
                    </span>
                    <span className="text-sm text-gray-400 line-through">
                      {product.oldPrice}
                    </span>
                  </div>
                </div>
              </div>
            ))}
          </div>
        </div>
      </section>

      {/* Categories Section */}
      <section className="py-12 bg-white dark:bg-[#1a1a1a]">
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <h2 className="text-3xl font-bold text-gray-900 dark:text-white mb-8">
            Shop by Category
          </h2>
          <div className="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-6 gap-4">
            {[
              { name: "MPPT Controllers", icon: "⚡" },
              { name: "Solar Inverters", icon: "🔌" },
              { name: "Power Supplies", icon: "🔋" },
              { name: "Lab Equipment", icon: "🔬" },
              { name: "Accessories", icon: "🛠️" },
              { name: "New Arrivals", icon: "✨" },
            ].map((category, index) => (
              <div
                key={index}
                className="bg-gray-50 dark:bg-[#0a0a0a] rounded-lg p-6 text-center hover:shadow-lg hover:bg-orange-50 dark:hover:bg-orange-900/20 transition-all cursor-pointer group"
              >
                <div className="text-4xl mb-3 group-hover:scale-110 transition-transform">
                  {category.icon}
                </div>
                <div className="text-sm font-medium text-gray-700 dark:text-gray-300">
                  {category.name}
                </div>
              </div>
            ))}
          </div>
        </div>
      </section>

      {/* Footer */}
      <footer className="bg-gray-900 text-white py-12">
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <div className="grid grid-cols-1 md:grid-cols-4 gap-8">
            <div>
              <h3 className="text-xl font-bold text-[#ff6a00] mb-4">MYAMi</h3>
              <p className="text-gray-400 text-sm">
                Professional solar and power solutions for your energy needs.
              </p>
            </div>
            <div>
              <h4 className="font-semibold mb-4">Products</h4>
              <ul className="space-y-2 text-sm text-gray-400">
                <li>
                  <a href="#" className="hover:text-[#ff6a00]">
                    MPPT Controllers
                  </a>
                </li>
                <li>
                  <a href="#" className="hover:text-[#ff6a00]">
                    Solar Inverters
                  </a>
                </li>
                <li>
                  <a href="#" className="hover:text-[#ff6a00]">
                    Power Supplies
                  </a>
                </li>
                <li>
                  <a href="#" className="hover:text-[#ff6a00]">
                    Lab Equipment
                  </a>
                </li>
              </ul>
            </div>
            <div>
              <h4 className="font-semibold mb-4">Support</h4>
              <ul className="space-y-2 text-sm text-gray-400">
                <li>
                  <a href="#" className="hover:text-[#ff6a00]">
                    Help Center
                  </a>
                </li>
                <li>
                  <a href="#" className="hover:text-[#ff6a00]">
                    Shipping Info
                  </a>
                </li>
                <li>
                  <a href="#" className="hover:text-[#ff6a00]">
                    Returns
                  </a>
                </li>
                <li>
                  <a href="#" className="hover:text-[#ff6a00]">
                    Warranty
                  </a>
                </li>
              </ul>
            </div>
            <div>
              <h4 className="font-semibold mb-4">Contact</h4>
              <ul className="space-y-2 text-sm text-gray-400">
                <li>📧 kafu@myami.cn</li>
                <li>📱 WhatsApp: +86 13532926513</li>
                <li>💬 WeChat: kafu-990407</li>
              </ul>
            </div>
          </div>
          <div className="border-t border-gray-800 mt-8 pt-8 text-center text-sm text-gray-400">
            © 2025 MYAMi Official Store. All rights reserved.
          </div>
        </div>
      </footer>
    </div>
  );
}
