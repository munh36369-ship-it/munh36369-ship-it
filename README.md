<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0F172A,45:14532D,100:0F766E&height=220&section=header&text=MOON%20HYEONGJUN&fontSize=48&fontColor=FFFFFF&fontAlignY=40&desc=Reinforcement%20Learning%20%7C%20Computer%20Vision%20%7C%20Research&descAlignY=65&descSize=17" width="100%" alt="Moon Hyeongjun Portfolio Header" />

### 문형준 | Moon Hyeongjun

**Computer Engineering · Hanbat National University**  
**Research Collaboration · Reinforcement Learning · Computer Vision**

[![GitHub Profile](https://img.shields.io/badge/GitHub-munh36369--ship--it-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/munh36369-ship-it)
[![Featured Research](https://img.shields.io/badge/Research-Craftax_Resource--Aware_Skill-0F766E?style=for-the-badge)](https://github.com/Gyeometry/Craftax-Resource-Aware-Skill)

</div>

---

## 👋 About Me

안녕하세요. 국립한밭대학교 컴퓨터공학과에서 소프트웨어 개발과 인공지능 관련 프로젝트를 수행하고 있는 **문형준**입니다.

강화학습 정책의 동작과 실패 원인을 분석하고, 실험을 통해 개선 효과를 검증하는 연구에 관심이 있습니다. 본 포트폴리오에서는 **Craftax 기반 강화학습 연구에 공동 연구자 및 논문 공동저자로 참여한 경험**을 중심으로 소개합니다.

**Research Interests**  
`Reinforcement Learning` · `Policy Evaluation` · `Skill Learning` · `Computer Vision` · `3D Point Cloud Processing`

---

## 🔬 Featured Research

### Craftax: Resource-Aware Skill Intervention for a Frozen PPO-RNN

[![Research](https://img.shields.io/badge/Type-Collaborative_Research-1F6FEB?style=flat-square)](https://github.com/Gyeometry/Craftax-Resource-Aware-Skill)
![Status](https://img.shields.io/badge/Status-Research_Project-64748B?style=flat-square)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![JAX](https://img.shields.io/badge/JAX-FF6F00?style=flat-square)
![PPO](https://img.shields.io/badge/PPO--RNN-334155?style=flat-square)

**공동 연구 프로젝트 | Co-researcher & Manuscript Co-author**  
**연구 저장소:** [Gyeometry/Craftax-Resource-Aware-Skill](https://github.com/Gyeometry/Craftax-Resource-Aware-Skill)  
**협업:** [Gyeom Kim (@Gyeometry)](https://github.com/Gyeometry)

#### 연구 배경

Craftax-Classic 환경에서 기존 **PPO-RNN** 정책을 재현하고 **Invalid Action Masking**을 적용한 뒤에도, 철 도구 제작에 필요한 자원을 확보했음에도 작업대·화로를 이용할 수 있는 상태를 제대로 구성하지 못하는 경우가 관찰되었습니다.

이 연구는 정책 전체를 다시 학습하지 않고도 이러한 **상태 구성(State Construction) 병목**을 보완하는 방법을 다룹니다.

#### 핵심 연구 방법

1. **Baseline & Invalid Action Masking**: 기존 PPO-RNN을 기반으로 실행 불가능한 행동을 정책 선택에서 제외하고 비교 평가합니다.
2. **Failure Analysis & Planner**: 철 도구 제작 과정을 자원 확보, 제작 가능 상태 구성, 실제 제작 행동으로 나눠 실패 원인을 분석합니다.
3. **Behavior-Cloned Skill**: 규칙 기반 Planner의 행동 시연으로 별도의 **CNN-GRU Skill Policy**를 학습합니다.
4. **Resource-Aware Initiation**: 도구 제작용 자원과 설비 설치 비용을 함께 고려하여 Skill의 시작 여부를 결정합니다.
5. **Frozen PPO-RNN Integration**: 기본 정책의 학습된 가중치를 고정한 채 Skill이 필요한 순간에만 개입하고, 상태 구성이 끝나면 기본 정책으로 제어권을 반환합니다.

#### 실험 결과

원본 저장소에서 보고한 **동일 평가 구성의 결과**입니다. 각 조건은 총 **4,096게임**에서 평가하였습니다.

| 평가 조건 | 평균 Raw Return | 마스킹 적용 기본 정책 대비 |
|:--|--:|--:|
| PPO-RNN + Invalid Action Masking | 14.26577 | 기준 |
| + Learned Skill | 14.39053 | +0.12476 |
| **+ Learned Skill + Resource-Aware Initiation** | **14.49502** | **+0.22925** |

같은 평가에서 철곡괭이 제작 업적은 **158 → 569**, 철검 제작 업적은 **151 → 653**으로 나타났습니다. 수치는 **팀 프로젝트 전체의 실험 결과**이며, 개인 단독 성과를 의미하지 않습니다.

#### System Architecture

<div align="center">
  <img src="https://raw.githubusercontent.com/Gyeometry/Craftax-Resource-Aware-Skill/main/assets/architecture.png" width="90%" alt="Craftax resource-aware skill intervention architecture" />
</div>

#### Research Contribution & Collaboration

- **참여 형태:** 공동 연구자 및 연구 논문 공동저자
- **연구 주제:** PPO-RNN의 상태 구성 실패 분석과 자원 인식형 Skill 개입
- **연구 범위:** 정책 비교, Skill 기반 상태 구성, 개입 조건, 실험 검증을 포함한 공동 연구
- **원본 코드 및 연구 기록:** [프로젝트 README](https://github.com/Gyeometry/Craftax-Resource-Aware-Skill#readme) · [프로젝트 수행 내역](https://github.com/Gyeometry/Craftax-Resource-Aware-Skill/blob/main/docs/PROJECT_WORK.md) · [실험 결과](https://github.com/Gyeometry/Craftax-Resource-Aware-Skill/blob/main/docs/RESULTS.md)

> **Attribution:** 이 항목은 공동 연구 프로젝트를 소개합니다. 구체적인 개인별 구현·실험 분담은 공동저자들과 확인한 기여 내역에 따라 별도로 명시하며, 공개된 저장소의 전체 코드를 개인 단독 저작물로 주장하지 않습니다.

> **Publication Status:** 연구 프로젝트와 논문 원고의 참여 이력을 소개하는 것으로, 학술지·학술대회 게재 확정이나 심사 통과를 주장하지 않습니다.

---

## 🧰 Technical Focus

| 분야 | 기술 및 접근 방법 |
|:--|:--|
| Reinforcement Learning | PPO-RNN, Invalid Action Masking, Policy Evaluation |
| Skill Learning | Behavior Cloning, CNN-GRU, Hierarchical Control |
| Experimentation | Ablation Study, Paired Evaluation, Reproducibility |
| Development | Python, JAX, Git, GitHub |

---

## 🔗 Research Links

- **공동 연구 저장소:** [Craftax-Resource-Aware-Skill](https://github.com/Gyeometry/Craftax-Resource-Aware-Skill)
- **협업 연구자:** [Gyeometry](https://github.com/Gyeometry)
- **GitHub:** [munh36369-ship-it](https://github.com/munh36369-ship-it)

<sub>Third-party Craftax/PPO code and original project implementation are subject to their respective licenses and notices. Refer to the [repository LICENSE](https://github.com/Gyeometry/Craftax-Resource-Aware-Skill/blob/main/LICENSE) and [third-party notices](https://github.com/Gyeometry/Craftax-Resource-Aware-Skill/blob/main/THIRD_PARTY_NOTICES.md). This profile README does not redistribute that code or grant additional permissions.</sub>

<div align="center">

---

**Understand the failure · Design the intervention · Verify the result**

</div>
