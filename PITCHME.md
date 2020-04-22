# Flux 

An application architecture for React

---

### Flux Design

- Dispatcher: Manages Data Flow
- Stores: Handle State & Logic
- Views: Render Data via React

---

![Flux Explained](https://facebook.github.io/flux/img/flux-simple-f8-diagram-explained-1300w.png)

---


    ```elixir
    defmodule GenMetrics.GenStage.Monitor do
        use GenServer

        alias GenMetrics.GenStage.Manager
        alias GenMetrics.GenStage.Monitor
        alias GenMetrics.GenStage.Pipeline
        alias GenMetrics.GenStage.Window
        alias GenMetrics.Reporter
        alias GenMetrics.Utils.Runtime

        @moduledoc false
        @handle_demand :handle_demand
        @handle_events :handle_events
        @handle_call   :handle_call
        @handle_cast   :handle_cast

        defstruct pipeline: %Pipeline{}, metrics: nil, start: 0, duration: 0
    ```
