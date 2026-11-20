# Browser Language Web Skill

[English](#english) · [한국어](#한국어)

## English

An agent Skill for building a website that follows the visitor's browser language, remembers a manual language choice, and keeps explicit language URLs working. It adapts to the site's existing framework and translation setup.

Ask your coding agent:

> Use `browser-language-web` to make this site available in Korean and English. Detect the browser language on a first visit, remember a manual choice, and keep language links working across pages.

### Install

Copy this repository's `SKILL.md` into your agent's Skill directory as `browser-language-web/SKILL.md`, then ask the agent to use `browser-language-web`. The exact Skill directory depends on your agent and whether you want project-wide or personal installation.

### What it checks

URL choice → saved manual choice → browser preference → fallback. It also covers full-page copy, document language, accessible controls, navigation, and locale-sensitive formatting.

The Skill guides an agent; it does not automatically translate a site or guarantee translation quality. Review the resulting copy and implementation.

### Measure the effect

Compare equivalent multilingual site tasks with and without this Skill using the same model and project. Check the first implementation against browser language selection, manual choice, URL override, fallback, navigation, accessibility, and untranslated copy. Report the first-pass completion rate (`requirements met ÷ applicable requirements × 100`) and the number of correction rounds. No measured improvement percentage is available yet.

## 한국어

방문자의 브라우저 언어에 맞춰 사이트를 보여주고, 직접 선택한 언어를 기억하며, URL로 지정한 언어도 유지하는 웹을 만들도록 돕는 에이전트 Skill입니다. 기존 프레임워크와 번역 구조에 맞춰 적용합니다.

코딩 에이전트에게 이렇게 요청하세요.

> `browser-language-web`을 사용해서 이 사이트를 한국어와 영어로 제공해줘. 첫 방문에는 브라우저 언어를 감지하고, 직접 고른 언어는 기억하며, 페이지를 이동해도 언어 링크가 유지되게 해줘.

### 설치

이 저장소의 `SKILL.md`를 사용하는 에이전트의 Skill 폴더에 `browser-language-web/SKILL.md`로 복사한 뒤, `browser-language-web`을 사용해 달라고 요청하세요. 폴더 위치는 에이전트와 프로젝트 단위·개인 단위 설치 여부에 따라 다릅니다.

### 확인 범위

URL 지정 → 저장된 직접 선택 → 브라우저 선호 언어 → 기본 언어 순서로 판단합니다. 페이지 전체 문구, 문서 언어, 접근 가능한 전환 버튼, 페이지 이동, 날짜·숫자 형식도 확인합니다.

이 Skill은 에이전트의 작업을 안내합니다. 번역을 자동으로 보증하지 않으므로 결과 문구와 구현을 직접 검토하세요.

### 효과 측정

같은 모델과 프로젝트에서 비슷한 다국어 사이트 작업을 Skill 사용 전후로 비교하세요. 첫 결과물의 브라우저 언어 선택, 직접 선택, URL 우선순위, 기본 언어, 페이지 이동, 접근성, 번역 누락을 확인합니다. 첫 결과물의 충족률(`충족한 요구사항 수 ÷ 적용되는 요구사항 수 × 100`)과 추가 수정 횟수를 함께 공개하세요. 아직 향상률 실측치는 없습니다.
