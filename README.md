 MapPulse ECO  — Real-Time Fleet & Energy Management System

A fault-tolerant, real-time fleet tracking and dynamic cost/energy consumption management system built with **.NET 8 API**, **SignalR**, **Dapper (SQLite)**, and **Leaflet.js**. Integrated with **OSRM (Open Source Routing Machine) API** to track vehicles precisely along actual streets and simulation constraints.   

 Key Features

- **True-to-Life Routing (OSRM Integration):** Vehicles don't just jump across points or move in straight lines; they follow precise streets, turns, and real driving routes using the OSRM routing engine.
- **Dynamic Fuel & Energy Telemetry:** Simulates real-time consumption based on distance and vehicle profiles:
  - **Electric Vehicles (EV):** Low per-KM cost with active battery drain monitoring.
  - **Internal Combustion Engine Vehicles (ICE):** Custom parameters for Motorcycles (Gasoline) and Heavy Trucks (Diesel).
- **Automated Smart Charging/Refueling:** If an electric vehicle's battery drops below **20%** during a live run, the system automatically overrides the current route, triggers an alert, and redirects the vehicle to the nearest smart charging station **(⚡)** to recover to 100%.
- **Live WebSocket Streaming:** High-performance, bi-directional telemetry streaming powered by **SignalR** to sync hardware stats (speed, battery, total accumulated cost, and trip distance) to the map instantly.
- **Lightweight Architecture:** Uses **Dapper ORM** and an asynchronous **SQLite** provider for blazing-fast database operations.

 Tech Stack & Architecture

- **Backend:** C# / .NET 8.0 Web API
- **Data Access:** Dapper (Micro-ORM) & Microsoft.Data.Sqlite
- **Real-Time Layer:** ASP.NET Core SignalR (WebSockets)
- **Frontend Engine:** Native HTML5 / CSS3 (Flexbox) / JavaScript (ES6)
- **GIS & Mapping:** Leaflet.js (Standard OSM Tile Layers)
- **Routing Engine:** OSRM Driving API



 MapPulse ECO  - Gerçek Zamanlı Filo ve Enerji Yönetim Sistemi

 Öne Çıkan Özellikler
Gerçek Rota ve Yol Navigasyonu (OSRM): Araçlar harita üzerinde düz çizgiler halinde değil; OSRM motorunu kullanarak gerçek sokak dönüşlerini, caddeleri ve tek yönleri analiz ederek ilerler.

Dinamik Enerji & Yakıt Telemetrisi: Kat edilen gerçek mesafeye göre araç türüne özel kümülatif maliyet hesaplaması yapar:

Elektrikli Otomobil (EV): KM başına düşük maliyet (0.8 TL) ve anlık batarya tüketim takibi.

İçten Yanmalı Araçlar: Motosiklet (Benzin - 1.5 TL/KM) ve Ağır Vasıta Kamyon (Dizel - 4.5 TL/KM) için farklı tüketim katsayıları.

Otonom Akıllı Şarj İstasyonu Yönlendirmesi: Görev halindeki elektrikli aracın şarjı %20'nin altına düştüğü an sistem rotayı otonom olarak keser, kullanıcıya uyarı fırlatır ve aracı haritadaki en yakın şarj istasyonuna (⚡) yönlendirerek bataryayı %100'e tamamlar.

Canlı WebSocket Akışı: SignalR altyapısı sayesinde araçların koordinat, anlık hız, kalan yakıt/enerji, toplam kat edilen yol (KM) ve toplam harcanan bütçe (TL) verileri haritada anlık olarak senkronize edilir.

Hafif ve Kararlı Veritabanı Mimarisi: Arka planda yüksek performanslı Dapper ORM ve asenkron SQLite kullanılarak telemetri verileri milisaniyeler içinde loglanır.

 Kullanılan Teknolojiler
Backend : C# / .NET 8.0 Web API

Veritabanı Katmanı: Dapper (Micro-ORM) & Microsoft.Data.Sqlite

Real-Time Protokolü: ASP.NET Core SignalR (WebSockets)

Frontend : Saf HTML5 / CSS3 (Flexbox) / JavaScript (ES6)

Harita Kütüphanesi: Leaflet.js & OpenStreetMap Katmanları

Yönlendirme Servisi: OSRM Driving API
