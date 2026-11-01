# EmbodiedAgent

**Agent-as-a-Service for embodied intelligence.**

EmbodiedAgent closes the perception-planning-action loop across simulation and physical environments with hard safety limits.

面向具身智能的 Agent：在仿真与真实环境中闭合感知、规划、行动回路，并以硬性安全边界控制物理执行。

## Agent loop

| Stage | Responsibility |
|---|---|
| Data | RGB-D, proprioception, trajectories, simulation logs |
| Models | Vision-language-action model, world model, spatial policy |
| Training | Imitation learning, simulation RL, Sim2Real adaptation |
| Inference | Low-latency perception, planning, action chunks |
| Harness | Robot SDK, simulator, safety envelope, fleet control |
| Eval | Task success, safety, robustness, sim-to-real gap |

## Initial scope

- Build a simulator-first development loop.
- Keep an independent safety governor around every action.
- Log observations, actions, failures, and recovery paths.

## Roadmap

- [ ] Robot and simulator adapter interfaces
- [ ] Imitation-learning baseline
- [ ] Safety governor
- [ ] Sim-to-real evaluation suite
- [ ] Fleet-level coordination

## Engineering principles

- Physical safety is never delegated to an LLM alone.
- Every action must be bounded and interruptible.
- Evaluate in the real world only after simulation gates pass.

