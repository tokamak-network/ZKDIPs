# ZKDIPs
ZK-DEX 개선제안(ZKDIPs)은 zk-dex 플랫폼의 코어 프로토콜, 클라이언트 api, 컨트랙트 구현의 표준을 기술한다.

# 기여 방법

 1. [ZKDIP-1](ZKDIPs/zkdip-1.md)을 먼저 살펴본다.
 2. 우측 상단에 포크(Fork) 버튼을 클릭.
 3. 개선제안을 ZKDIP 포크 저장소에 포함시킨다. [ZKDIP 템플릿](../zkdip-template.md) 참조.
 4. [ZKDIPs repository](https://github.com/Onther-Tech/ZKDIPs)에 풀 리퀘스트 요청.

첫번째 풀 리퀘스트(이하 PR)은 최종(Final) PR의 첫번째 초안(Draft)이 된다. PR은 정해진 템플릿을 따라야 한다. 편집()(editor)는 ZKDIP의 PR을 검토하고 병합(merge)하기 전 ZKDIP 번호를 부여한다. 여기서 중요한 사항은 PR의 `discussions-to` 헤더에 깃헙 이슈 URL을 포함하여 사람들이 해당 제안에 대해서 공개적으로 토론할 수 있도록 만드는 것이다.

만약 ZKDIP에 이미지가 포함되어야 한다면, 이미지 파일은 `assets` 디렉토리에 `assets/zkdip-N` 내부에 포함되어야 한다 (향후에 **N** 은 ZKDIP번호로 대체될 수 있다). ZKDIP에 이미지를 포함할때는 `../assets/zkdip-1/image.png`와 같은 상대경로를 사용해야 한다.

만약 ZKDIP가 충분히 검토를 마쳐서 초안 이후의 단계로 넘어갈 수 있다고 생각되면, 다음 두가지 중 하나를 택해서 수행해야 한다.

 - **ZKDIP의 코어 프로토콜과 관련된 것**, [이 캘린더](https://calendar.google.com/calendar/embed?src=onther.io_r5sqccaoqrrjfio3nli8bpbk34%40group.calendar.google.com&ctz=Asia%2FSeoul)에 온더의 코어팀과 세미나를 열고 향후 업그레이드에 반영될 수 있도록 토의를 한다. 토의를 거쳐서 이 부분이 충분히 반영될 수 있다고 판단하면, 편집자(editor)는 ZKDIP를 최종(Final) 상태로 바꾼다.
 - **기타 ZKDIP**, ZKDIP의 상태를 '최종(Final)' 상태로 바꾸는 PR을 연다. 편집자는 초안(draft)를 검토하고, 누구도 반대하지 않으면 해당 ZKDIP를 최종(final)상태로 바꾼다. 만약 편집자가 해당 안에 대해서 합의가 이뤄지지 않는다고 판단하면 - 예를들어 다른 기여자 혹은 다른 편집자 중 한명이 심각한 기술적인 오류 등을 지적하면 - 해당 PR은 닫히게(close) 된다. 제안자(author)는 이러한 부분을 수정하고 다시 PR을 만들어야 한다.

# ZKDIP 상태(status) 정의

* **초안(Draft)** - an ZKDIP가 피드백 및 리뷰를 받고 있으며, 지속적인 개선이 일어나고 있는 상태.
* **최종(Final (non-Core))** - ZKDIP는 더이상 기술적인 변경 사항이 없으며, 모든 기술적인 사항들은 제안자(author)에 의해 해결된 상태.
* **최종(Final (Core))** - ZKDIP가 zk-dex 코어팀에 의해서 향후 업그레이드에 반영될 것으로 결정되었거나, 이미 포함된 상태.
