# [NextEdge Deusto](https://github.com/NextEdge-Deusto)

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&height=220&color=0:0f172a,50:1d4ed8,100:22c55e&text=NextEdge%20Deusto&fontColor=ffffff&fontAlignY=38&desc=Copilots,%20mobility,%20AI%20services%20and%20connected%20products&descAlignY=58" alt="NextEdge Deusto banner" />
</p>

<p align="center">
  <a href="https://github.com/NextEdge-Deusto">
    <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&pause=1600&color=38BDF8&center=true&vCenter=true&width=900&lines=Building+connected+copilots+for+real+operations;Frontend%2C+backend+and+microservices+in+active+development;Mobility%2C+telematics%2C+calendar+intelligence+and+assistant+workflows" alt="Typing intro" />
  </a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/status-active%20development-22c55e?style=for-the-badge" alt="Active development" />
  <img src="https://img.shields.io/badge/architecture-microservices-0ea5e9?style=for-the-badge" alt="Microservices" />
  <img src="https://img.shields.io/badge/frontend-mobile%20%2B%20desktop-f59e0b?style=for-the-badge" alt="Frontend apps" />
  <img src="https://img.shields.io/badge/backend-gateway%20%2B%20domain%20services-1d4ed8?style=for-the-badge" alt="Backend services" />
</p>

## Qué Construye Esta Organización

NextEdge Deusto está evolucionando desde repos aislados hacia un ecosistema de producto conectado.  
Ahora mismo el foco principal de desarrollo está en los repos **`next_frontend`** y **`next_service`**, donde se está construyendo la plataforma central con:

- un **panel desktop** para operación y monitorización,
- una **app móvil de conducción** para sesiones en vivo y flujos de asistente,
- un **backend dividido en microservicios de dominio** detrás de un gateway,
- y varios repos satélite para telemetría, ranking, asistentes, calendario y exploración de datos.

La idea ya no es una demo suelta. La dirección es una **plataforma componible** donde copilots, telemetría, eventos, compliance y datos operativos trabajan juntos.

## Plataforma Principal Actual

### `next_frontend`
- **App desktop de administración** con Vue 3, Vite, Tailwind y ECharts.
- **App móvil de conducción** con Nuxt 4, PWA, mapas y experiencia live trip.
- Paquete compartido para tipos, auth, acceso a API y contratos WebSocket.

### `next_service`
- Gateway backend expuesto en `:8000`.
- Servicios de dominio para:
  - `assistant`
  - `auth`
  - `calendar`
  - `compliance`
  - `gasolineras`
  - `ingest`
  - `scoring`
  - `speedlimit`
  - `worker`

## Forma del Sistema

```mermaid
flowchart LR
  M[App movil<br/>driving experience] --> G[Gateway API]
  D[Desktop Admin<br/>operations view] --> G
  G --> A[Assistant]
  G --> C[Calendar]
  G --> S[Scoring]
  G --> P[Compliance]
  G --> L[Speed Limit]
  G --> I[Ingest]
  G --> F[Gas Stations]
  G --> W[Workers]
  I --> T[(Telemetry / datasets)]
  C --> E[(Events / schedule context)]
  S --> R[(Driving insights)]
```

## Repos del Ecosistema

<table>
  <tr>
    <td width="50%">
      <a href="https://github.com/NextEdge-Deusto/next_frontend">
        <img src="https://github-readme-stats.vercel.app/api/pin/?username=NextEdge-Deusto&repo=next_frontend&theme=transparent" alt="next_frontend repo card" />
      </a>
    </td>
    <td width="50%">
      <a href="https://github.com/NextEdge-Deusto/next_service">
        <img src="https://github-readme-stats.vercel.app/api/pin/?username=NextEdge-Deusto&repo=next_service&theme=transparent" alt="next_service repo card" />
      </a>
    </td>
  </tr>
  <tr>
    <td width="50%">
      <a href="https://github.com/NextEdge-Deusto/next_copilot">
        <img src="https://github-readme-stats.vercel.app/api/pin/?username=NextEdge-Deusto&repo=next_copilot&theme=transparent" alt="next_copilot repo card" />
      </a>
    </td>
    <td width="50%">
      <a href="https://github.com/NextEdge-Deusto/next_assistant">
        <img src="https://github-readme-stats.vercel.app/api/pin/?username=NextEdge-Deusto&repo=next_assistant&theme=transparent" alt="next_assistant repo card" />
      </a>
    </td>
  </tr>
  <tr>
    <td width="50%">
      <a href="https://github.com/NextEdge-Deusto/driving-ranking">
        <img src="https://github-readme-stats.vercel.app/api/pin/?username=NextEdge-Deusto&repo=driving-ranking&theme=transparent" alt="driving-ranking repo card" />
      </a>
    </td>
    <td width="50%">
      <a href="https://github.com/NextEdge-Deusto/dashboard">
        <img src="https://github-readme-stats.vercel.app/api/pin/?username=NextEdge-Deusto&repo=dashboard&theme=transparent" alt="dashboard repo card" />
      </a>
    </td>
  </tr>
  <tr>
    <td width="50%">
      <a href="https://github.com/NextEdge-Deusto/calendar_labs">
        <img src="https://github-readme-stats.vercel.app/api/pin/?username=NextEdge-Deusto&repo=calendar_labs&theme=transparent" alt="calendar_labs repo card" />
      </a>
    </td>
    <td width="50%">
      <a href="https://github.com/NextEdge-Deusto/calendar_models">
        <img src="https://github-readme-stats.vercel.app/api/pin/?username=NextEdge-Deusto&repo=calendar_models&theme=transparent" alt="calendar_models repo card" />
      </a>
    </td>
  </tr>
</table>

## Líneas de Trabajo

| Área | Qué está pasando ahora |
|---|---|
| Producto principal | `next_frontend` y `next_service` concentran la evolución de la plataforma |
| Copilot UX | Experiencia dual: escritorio de operación + asistente móvil en vivo |
| Movilidad | Contexto de ruta, viaje, gasolineras y soporte al conductor |
| Inteligencia de calendario | Comprensión de eventos y predicción de desplazamiento |
| Telemetría | Exploración, limpieza y extracción de señales del dataset |
| Scoring | Análisis de calidad de conducción y compliance |
| Plataforma | Backend con gateway y descomposición por servicios |

## Snapshot Técnico

<p align="center">
  <img height="170" src="https://github-readme-stats.vercel.app/api?username=NextEdge-Deusto&show_icons=true&theme=transparent&hide_border=true" alt="GitHub stats" />
  <img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=NextEdge-Deusto&layout=compact&theme=transparent&hide_border=true" alt="Top languages" />
</p>

## Por Qué Existe Este README

Este perfil es la puerta de entrada de la organización. Tiene que explicar la plataforma, no solo un modelo o un experimento concreto.  
Los repos de aquí representan capas distintas de una misma dirección: **copilots que combinan producto, APIs operativas, señales del mundo real y AI aplicada**.

---

<p align="center">
  <sub>README de perfil mantenido como mapa público de la organización mientras la plataforma sigue evolucionando.</sub>
</p>
