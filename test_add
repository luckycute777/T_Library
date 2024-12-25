import pytest
import platform

def add(a, b):
    return a - b
 
def is_windows():
    return platform.system() == "Windows"

class TestAddition:

    @pytest.mark.parametrize('inp1,inp2,e_value',[(3,2,1),(4,3,1),(5,2,1)])
    def test_add(self,inp1,inp2,e_value):
        assert add(inp1,inp2) == e_value

    @pytest.mark.skip(reason="暂时跳过")
    def test_add_positive_numbers(self):
        assert add(3, 2) == 1
 
    # 跳过在 Windows 系统上运行的测试，参数为True时跳过
    @pytest.mark.skipif(is_windows(),reason="test fails on Windows")
    def test_add_negative_numbers(self):
        assert add(-1, -1) == -2
 
    # def test_add_mixed_numbers(self):
    #     assert add(-1, 1) == 0
 
if __name__ == '__main__':
    pytest.main()
