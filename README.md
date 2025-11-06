# CommandProjectPV-425  
**Система измерения производительности параллельных алгоритмов на платформе .NET**

> Курсовой проект группы ПВ-425 по дисциплине «Программирование на платформе .NET»

![.NET 8](https://img.shields.io/badge/.NET-8.0-blue)
![WPF](https://img.shields.io/badge/UI-WPF-purple)
![MVVM + DI](https://img.shields.io/badge/Architecture-MVVM%20%2B%20DI-green)
![SQLite](https://img.shields.io/badge/Database-SQLite-lightgrey)

---

## 📌 Описание проекта

WPF-приложение для объективного сравнения производительности **9 методов выполнения** (.NET TPL, PLINQ, SIMD и др.) при решении **5 вычислительных задач** на массивах.  
Результаты замеряются через **BenchmarkDotNet**, отображаются в виде **интерактивных графиков**, сохраняются в **SQLite** и могут экспортироваться в **JSON**.

Архитектура: **MVVM + Dependency Injection + Entity Framework Core**.

---

## 🗃 Структура проекта
CommandProjectPV-425/
├── Helpers/ # Вспомогательные утилиты (JsonHelper, SystemInfo)
├── Interfaces/ # IBenchmarkService, IChartService, IDataService
├── Models/ # BenchmarkResult.cs, AppDbContext.cs
├── Services/ # Реализации сервисов
├── Tests/ # Бенчмарки: CountAboveAverage.cs, FindPrimeNumbers.cs и др.
├── ViewModels/ # MainViewModel.cs, ChartViewModel.cs
├── Views/ # MainWindow.xaml, ChartView.xaml
├── App.xaml # Точка входа WPF
├── App.xaml.cs # Регистрация DI и запуск
└── bin/Debug/net8.0/Data/app.db ← БД создаётся автоматически при первом запуске
