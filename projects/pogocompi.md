---
layout: default
title: PoGoCompi - Comparador DPS Pokémon GO - Álvaro González  
description: Herramienta web para análisis competitivo de Pokémon GO con cálculos de DPS e IVs client-side
---

# 📊 PoGoCompi

[← Volver al portafolio](../)

## 📋 Descripción del Proyecto

**Herramienta web avanzada para análisis competitivo de Pokémon GO** que permite comparar DPS (Damage Per Second) y evaluar IVs (Individual Values) con cálculos completamente realizados en el cliente. Inspirado en la metodología de PvPoke, ofrece análisis detallado para optimización competitiva.

## ✨ Características Principales

### 📈 Análisis de DPS Avanzado
- **Cálculos precisos de DPS** basados en estadísticas reales del juego
- **Comparación de movesets** - Análisis de diferentes combinaciones de ataques
- **Simulaciones de combate** - Predicción de resultados en diferentes escenarios
- **Gráficos interactivos** - Visualización clara de datos de rendimiento

### 🎯 Evaluación de IVs
- **Calculadora de IVs** integrada para evaluación precisa
- **Ranking de IVs** - Ordenamiento por potencial competitivo
- **Análisis de breakpoints** - Puntos críticos de ataque y defensa
- **Optimización para Ligas** - Cálculos específicos para Great, Ultra y Master League

### 💾 Arquitectura Client-Side
- **100% client-side processing** - Todos los cálculos se realizan en el navegador
- **Sin dependencias de servidor** - Funciona completamente offline
- **LocalStorage integration** - Persistencia de datos y configuraciones
- **PWA ready** - Instalable como aplicación web progresiva

## 🛠️ Stack Tecnológico

```javascript
// Tecnologías principales
const TECH_STACK = {
    frontend: {
        framework: "React",
        language: "JavaScript ES6+", 
        styling: "CSS3 + Modules",
        charts: "Chart.js / D3.js"
    },
    
    data: {
        storage: "LocalStorage API",
        processing: "Vanilla JavaScript",
        source: "PogoAPI.net integration"
    },
    
    architecture: {
        type: "Single Page Application",
        pattern: "Component-based",
        state: "React Hooks",
        routing: "React Router"
    }
}
```

## 🎮 Funcionalidades Core

### **1. Comparador de DPS**
```javascript
// Ejemplo de cálculo de DPS
function calculateDPS(pokemon, moves, ivs, level) {
    const attack = getAttackStat(pokemon, ivs, level);
    const fastMove = moves.fast;
    const chargedMove = moves.charged;
    
    const cycle = calculateOptimalCycle(fastMove, chargedMove);
    const damage = calculateDamage(attack, cycle);
    
    return damage / cycle.duration;
}
```

### **2. Análisis de Movesets**
- **Database completa** de todos los movimientos de Pokémon GO
- **Cálculo de STAB** (Same Type Attack Bonus)
- **Efectividad de tipos** - Matriz completa de ventajas/desventajas
- **Análisis temporal** - Duración de ataques y ventanas de daño

### **3. Simulador de Combate**
- **Simulaciones 1v1** entre cualquier par de Pokémon
- **Scenarios múltiples** - Diferentes niveles y IVs
- **Weather effects** - Impacto del clima en el rendimiento
- **Shield scenarios** - Simulación con uso de escudos en PvP

## 📊 Interface de Usuario

### **Dashboard Principal**
```react
// Estructura del componente principal
const PoGoCompi = () => {
    return (
        <div className="dashboard">
            <PokemonSelector />
            <IVCalculator />
            <DPSComparator />
            <MovesetsAnalyzer />
            <ResultsChart />
        </div>
    );
};
```

### **Visualización de Datos**
- **Gráficos de barras** - Comparación visual de DPS
- **Tablas ordenables** - Rankings detallados
- **Heatmaps** - Efectividad de tipos visual
- **Progress indicators** - Cálculo de IVs en tiempo real

## 🔬 Algoritmos de Cálculo

### **Fórmula de Daño Base**
```javascript
const calculateBaseDamage = (attack, move, weather = 1.0) => {
    const power = move.power;
    const stab = move.type === pokemon.type ? 1.2 : 1.0;
    const effectiveness = getTypeEffectiveness(move.type, target.types);
    
    return Math.floor(
        (attack * power * stab * effectiveness * weather) / 100
    ) + 1;
};
```

### **Optimización de Ciclos de Ataque**
- **Fast move cycles** - Cálculo de energía generada
- **Charged move timing** - Optimización de uso de ataques cargados
- **TDO calculation** - Total Damage Output en raids
- **Battle rating** - Score competitivo general

## 📱 PWA Features

### **Instalación y Offline**
```javascript
// Service Worker para funcionalidad offline
self.addEventListener('fetch', event => {
    if (event.request.destination === 'document') {
        event.respondWith(
            caches.match('/index.html')
        );
    }
});
```

### **Características PWA**
- **Instalable** desde cualquier navegador
- **Funcionamiento offline** completo
- **Updates automáticos** de la base de datos
- **Responsive design** - Optimizado para móviles

## 🎯 Casos de Uso

### **Para Jugadores Competitivos**
- Optimización de equipos para GO Battle League
- Análisis de meta actual y predicción de cambios
- Preparación para torneos y competiciones

### **Para Raid Coordinators**
- Cálculo de DPS óptimo para raids
- Recomendaciones de equipos para diferentes jefes
- Análisis de breakpoints para maximizar daño

### **Para Collectors**
- Evaluación de IVs para decisiones de evolución
- Identificación de Pokémon con mayor potencial
- Optimización de recursos (dulces, polvos estelares)

## 🔧 Instalación y Uso

### **Acceso Web**
```bash
# Clonar repositorio
git clone https://github.com/4rgs/PoGoCompi.git
cd PoGoCompi

# Instalar dependencias
npm install

# Ejecutar en desarrollo
npm run dev

# Build para producción
npm run build
```

### **Hosting Estático**
El proyecto está optimizado para deployment en:
- GitHub Pages
- Netlify
- Vercel
- Cualquier hosting de archivos estáticos

## 📈 Roadmap

- [ ] **Integration con PokeGenie** - Import de IVs automático
- [ ] **Team builder** - Constructor de equipos optimizados  
- [ ] **Meta analysis** - Tracking de tendencias competitivas
- [ ] **Multi-language** - Soporte para múltiples idiomas
- [ ] **Advanced filters** - Filtros complejos para búsquedas
- [ ] **Share teams** - Sistema de compartir configuraciones

## 🔗 Enlaces

- **[📁 Repositorio GitHub](https://github.com/4rgs/PoGoCompi)**
- **[🌐 Demo en Vivo](https://4rgs.github.io/PoGoCompi)** *(si está deployado)*
- **[📚 Documentación](https://github.com/4rgs/PoGoCompi/wiki)**
- **[🐛 Reportar Issues](https://github.com/4rgs/PoGoCompi/issues)**

## 🏷️ Tags

`#PokemonGO` `#React` `#JavaScript` `#PWA` `#Gaming` `#Analytics` `#LocalStorage` `#ClientSide` `#DPS` `#IVs`

---

[← Volver al portafolio](../) | [🔗 Ver en GitHub](https://github.com/4rgs/PoGoCompi)