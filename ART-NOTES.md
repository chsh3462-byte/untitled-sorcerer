# v2.5 픽셀 스프라이트 제작 기록

제작 방식: 내장 imagegen 이미지 생성 도구로 새 그림을 만든 뒤, 투명 시트의 캐릭터 영역을 분리하고 게임용 픽셀 크기로 정규화했습니다. 외부에서 찾은 그림을 게임 자산으로 복사하지 않았습니다. 원본 PNG 4개(고죠 전용 보정 포함)와 최적화한 WebP 아틀라스 3개를 이 폴더에 보관합니다. 게임에는 WebP를 내장하여 인터넷 이미지 서버 없이 작동합니다.

외형 참고 검색: [애니메이션 공식 캐릭터 자료](https://jujutsukaisen.jp/character/category4.php), [공식 캐릭터 목록](https://jujutsukaisen.jp/character/). 호장 등 외형이 확정되지 않은 식신과 일반 주령은 게임용 해석입니다. 공식 원화를 그대로 재현한 자료가 아닌 비공식 팬 아트입니다.

## 최종 제작 프롬프트 세트

공통: “Production-ready Jujutsu Kaisen pixel-art sprite atlas. Full body, recognizable character anatomy, faces, hair, clothes and weapons. Premium 32-bit fighting game pixel art, crisp square pixel clusters, controlled color shading, not chibi. Transparent alpha background, no lettering, no panels, no scenery. Preserve ordering and separate every character inside its own cell.”

술사: 4열 × 5행. 쿠사카베, 노바라, 나나미, 토도 / 마키, 이누마키, 쵸소, 나오야 / 게토, 우라우메, 메구미, 이타도리 육체의 스쿠나 / 마히토, 유키, 고죠, 옷코츠 / 하카리, 토우지, 네 팔 스쿠나, 육안 고죠. 교복·안대·주언 옷깃·주구와 개별 전투 자세를 지정.

주령·보스: 4열 × 5행. 긴팔, 다안 군집, 그림자, 질식 / 저격수, 암살자, 괴뢰사, 손가락 수육체 / 포창신, 쿠로우루시, 죠고, 하나미 / 전투형 다곤, 마히토, 토우지, 카시모 / 켄자쿠, 네 팔 스쿠나, 리카, 창작 갑옷 주령. 원작 인물은 신체 특징과 복장을 개별 지정. 마지막 두 칸은 예비 그림이며 현재 게임의 적 목록에는 추가되지 않음.

식신: 4열 × 3행. 옥견 흑·백, 누에, 대사, 두꺼비 / 만상, 탈토, 원록, 관우 / 호장, 마허라, 옥견 혼, 가루다. 동물의 골격·깃털·비늘·털과 마허라의 법진을 지정. 마지막 두 칸은 예비 그림.

보정 요청: “Preserve all character identities and exact ordering. Shrink each sprite within its cell with transparent gutters; no neighboring sprites should overlap. Convert to genuine detailed 128-pixel-scale art with conspicuous square clusters, limited deliberate color shading and no antialiasing. Preserve full bodies and weapons.”

게임용 아틀라스는 칸당 176×192이며 캐릭터 최대 영역은 160×176입니다. 전투 모션은 기존 이동·피격·집중 연출을 유지하며 프레임별 신체 애니메이션을 새로 만든 것은 아닙니다.
