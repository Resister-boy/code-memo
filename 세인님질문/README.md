### 요구 사항

1. 사용자가 EOA에서 컨트렉트로 코인을 송금하면 사용자가 송금한 EOA로 token을 보내고 싶습니다.
2. 검색했을 때 receive()를 넣으면 컨트렉트가 코인을 받을 수 있고 receive() 함수 내부에 로직을 넣을 수 있다고 해서 아래와 같이 작업을 했습니다.

![image](https://github.com/Resister-boy/code-memo/assets/104838360/5ce8e03d-6083-4d11-b3b6-abcdc625a1dc)

```solidity
contract MyContract {
	
	receive() external payable {
	  mint(_msgSender());
	}
	 
	function mint(address _user) public returns (bool) {
		// mint
	}
}
```

### 질문

1. 요구 사항을 구현할 때 보통 위와 같이 구현을 하는지 궁금합니다.
2. 만약에 위와 같은 방법이 아니라면 어떤 방법을 사용하는지 궁금합니다.
