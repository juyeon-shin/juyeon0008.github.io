---
title : '02_4.Pandas 데이터프레임 변경' 
permalink: /PROGRAMMERS/02_4.Pandas데이터프레임변경/
excerpt : "02.데이터 다듬기/02_4.Pandas데이터프레임변경"
#categories : "KT_AIVLE_SCHOOL"
# tag : #"github.io"
date : '2023-09-18'

toc : True
toc_labels: True
toc_sticky : True
---

{
 "cells": [
  {
   "cell_type": "markdown",
   "id": "4d72cfe9",
   "metadata": {},
   "source": [
    "### day 1"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "fffcd8ca",
   "metadata": {},
   "source": [
    "#### 두 수의 합"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 1,
   "id": "6f344730",
   "metadata": {
    "ExecuteTime": {
     "end_time": "2023-08-01T13:15:42.807465Z",
     "start_time": "2023-08-01T13:15:42.788218Z"
    }
   },
   "outputs": [],
   "source": [
    "#두 수의 합\n",
    "def solution(num1, num2):\n",
    "    answer = num1+num2\n",
    "    return answer"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "8046184e",
   "metadata": {},
   "source": [
    "#### 두 수의 차"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 2,
   "id": "212d87b7",
   "metadata": {
    "ExecuteTime": {
     "end_time": "2023-08-01T13:15:42.823041Z",
     "start_time": "2023-08-01T13:15:42.810468Z"
    }
   },
   "outputs": [],
   "source": [
    "#두 수의 차\n",
    "def solution(num1, num2):\n",
    "    answer = num1-num2\n",
    "    return answer"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "6216b1ac",
   "metadata": {},
   "source": [
    "#### 두 수의 곱"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 3,
   "id": "f4b03986",
   "metadata": {
    "ExecuteTime": {
     "end_time": "2023-08-01T13:15:42.837989Z",
     "start_time": "2023-08-01T13:15:42.824977Z"
    }
   },
   "outputs": [],
   "source": [
    "#두 수의 곱\n",
    "def solution(num1, num2):\n",
    "    answer = num1*num2\n",
    "    return answer"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "69f4a067",
   "metadata": {},
   "source": [
    "#### 몫 구하기"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 4,
   "id": "5d977b45",
   "metadata": {
    "ExecuteTime": {
     "end_time": "2023-08-01T13:15:42.852985Z",
     "start_time": "2023-08-01T13:15:42.841996Z"
    }
   },
   "outputs": [],
   "source": [
    "#몫 구하기\n",
    "def solution(num1, num2):\n",
    "    answer = num1//num2\n",
    "    return answer"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "9af0b0c4",
   "metadata": {},
   "source": [
    "### day 2"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "df780784",
   "metadata": {},
   "source": [
    "#### 두 수의 나눗셈"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 5,
   "id": "12f11345",
   "metadata": {
    "ExecuteTime": {
     "end_time": "2023-08-01T13:15:42.867978Z",
     "start_time": "2023-08-01T13:15:42.856026Z"
    }
   },
   "outputs": [],
   "source": [
    "#두 수의 나눗셈\n",
    "def solution(num1, num2):\n",
    "    answer = num1/num2*1000\n",
    "    return int(answer)"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "1a865501",
   "metadata": {},
   "source": [
    "#### 숫자 비교하기"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 6,
   "id": "4c88847f",
   "metadata": {
    "ExecuteTime": {
     "end_time": "2023-08-01T13:15:42.883008Z",
     "start_time": "2023-08-01T13:15:42.871978Z"
    }
   },
   "outputs": [],
   "source": [
    "#숫자 비교하기\n",
    "def solution(num1, num2):\n",
    "    if num1 == num2:\n",
    "        answer = 1\n",
    "        \n",
    "    else:\n",
    "        answer = -1\n",
    "    return answer"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "7e6195c8",
   "metadata": {},
   "source": [
    "#### 분수의 덧셈"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 7,
   "id": "0605ffbe",
   "metadata": {
    "ExecuteTime": {
     "end_time": "2023-08-01T13:15:42.897979Z",
     "start_time": "2023-08-01T13:15:42.885980Z"
    }
   },
   "outputs": [],
   "source": [
    "#분수의 덧셈\n",
    "def solution(numer1, denom1, numer2, denom2):\n",
    "    import math\n",
    "    answer = []\n",
    "    \n",
    "    numer3 = numer1*denom2 + numer2*denom1 #분자\n",
    "    denom3 = denom1*denom2 #분모\n",
    "    gcd = math.gcd(numer3,denom3)\n",
    "    \n",
    "    answer.append(int(numer3/gcd))\n",
    "    answer.append(int(denom3/gcd))\n",
    "    \n",
    "    return answer"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 8,
   "id": "3d237591",
   "metadata": {
    "ExecuteTime": {
     "end_time": "2023-08-01T13:15:42.913001Z",
     "start_time": "2023-08-01T13:15:42.899976Z"
    }
   },
   "outputs": [
    {
     "data": {
      "text/plain": [
       "[29, 6]"
      ]
     },
     "execution_count": 8,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "#solution(1,2,3,4)\n",
    "solution(9,2,1,3)"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "855b58c1",
   "metadata": {},
   "source": [
    "#### 배열 2배 만들기"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 9,
   "id": "1f0ff892",
   "metadata": {
    "ExecuteTime": {
     "end_time": "2023-08-01T13:15:42.928523Z",
     "start_time": "2023-08-01T13:15:42.916002Z"
    }
   },
   "outputs": [],
   "source": [
    "#배열 2배 만들기\n",
    "#import numpy as np\n",
    "#np.dot([1,2,3,4],2)\n",
    "\n",
    "def solution(numbers):\n",
    "    answer = []\n",
    "    for i in range(len(numbers)):\n",
    "        numbers[i] = numbers[i]*2\n",
    "        \n",
    "    answer = numbers\n",
    "    return answer"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "944e7ff0",
   "metadata": {},
   "source": [
    "### day 3"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "e195a364",
   "metadata": {},
   "source": [
    "#### 나머지 구하기"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 10,
   "id": "684c672f",
   "metadata": {
    "ExecuteTime": {
     "end_time": "2023-08-01T13:15:42.943528Z",
     "start_time": "2023-08-01T13:15:42.933526Z"
    }
   },
   "outputs": [],
   "source": [
    "#나머지 구하기\n",
    "def solution(num1, num2):\n",
    "    answer = num1 %num2\n",
    "    return answer"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 11,
   "id": "e8ba0374",
   "metadata": {
    "ExecuteTime": {
     "end_time": "2023-08-01T13:15:42.973537Z",
     "start_time": "2023-08-01T13:15:42.951524Z"
    }
   },
   "outputs": [],
   "source": [
    "#중앙값 구하기\n",
    "def solution(array):\n",
    "    array = sorted(array)\n",
    "    answer = array[len(array)//2]\n",
    "    return answer"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 12,
   "id": "f24a3d09",
   "metadata": {
    "ExecuteTime": {
     "end_time": "2023-08-01T13:15:42.988526Z",
     "start_time": "2023-08-01T13:15:42.978527Z"
    }
   },
   "outputs": [],
   "source": [
    "#최빈값 구하기\n",
    "def solution(array):\n",
    "    answer = 0\n",
    "    an_dict = {}\n",
    "\n",
    "    for i in array:\n",
    "        if i in an_dict.keys():\n",
    "            an_dict[i] = an_dict[i] + 1\n",
    "        else:\n",
    "            an_dict[i] =  1\n",
    "\n",
    "    an_list = [k for k,v in an_dict.items() if v == max(an_dict.values())]\n",
    "\n",
    "    if len(an_list) != 1:\n",
    "        answer = -1\n",
    "    else:\n",
    "        answer = an_list[0]\n",
    "    \n",
    "    return answer"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 13,
   "id": "b66eae79",
   "metadata": {
    "ExecuteTime": {
     "end_time": "2023-08-01T13:15:43.004423Z",
     "start_time": "2023-08-01T13:15:42.993877Z"
    }
   },
   "outputs": [],
   "source": [
    "#짝수는 싫어요\n",
    "def solution(n):\n",
    "    answer = []\n",
    "    \n",
    "    for i in range(1,n+1,2):\n",
    "        answer.append(i)\n",
    "    return answer"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "a87ec598",
   "metadata": {},
   "source": [
    "### day 4"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 14,
   "id": "40e6803f",
   "metadata": {
    "ExecuteTime": {
     "end_time": "2023-08-01T13:15:43.019473Z",
     "start_time": "2023-08-01T13:15:43.008422Z"
    }
   },
   "outputs": [],
   "source": [
    "#피자 나눠 먹기 (1)\n",
    "def solution(n):\n",
    "    answer = n//7\n",
    "    \n",
    "    if n%7 !=0:\n",
    "        answer += 1\n",
    "    \n",
    "    return answer"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 15,
   "id": "62f94acd",
   "metadata": {
    "ExecuteTime": {
     "end_time": "2023-08-01T13:15:43.034326Z",
     "start_time": "2023-08-01T13:15:43.022223Z"
    }
   },
   "outputs": [],
   "source": [
    "#피자 나눠 먹기 (2)\n",
    "def solution(n):\n",
    "    answer = 6\n",
    "    \n",
    "    while answer%n != 0:\n",
    "        answer += 6\n",
    "    answer = answer//6\n",
    "    \n",
    "    return answer"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 16,
   "id": "c1f8571d",
   "metadata": {
    "ExecuteTime": {
     "end_time": "2023-08-01T13:15:43.049236Z",
     "start_time": "2023-08-01T13:15:43.038224Z"
    }
   },
   "outputs": [],
   "source": [
    "#피자 나눠 먹기 (3)\n",
    "def solution(slice, n):\n",
    "    answer = n//slice\n",
    "    hall = n%slice\n",
    "    if hall != 0:\n",
    "        answer += 1\n",
    "    return answer"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 17,
   "id": "a2378a0f",
   "metadata": {
    "ExecuteTime": {
     "end_time": "2023-08-01T13:15:43.064274Z",
     "start_time": "2023-08-01T13:15:43.053232Z"
    }
   },
   "outputs": [],
   "source": [
    "#배열의 평균값\n",
    "def solution(numbers):\n",
    "    answer = sum(numbers)/len(numbers)\n",
    "    return answer"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "22892f30",
   "metadata": {
    "ExecuteTime": {
     "end_time": "2023-08-01T13:14:57.967785Z",
     "start_time": "2023-08-01T13:14:57.944237Z"
    }
   },
   "source": [
    "### day 5"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 18,
   "id": "83a4ab2f",
   "metadata": {
    "ExecuteTime": {
     "end_time": "2023-08-01T13:21:29.845898Z",
     "start_time": "2023-08-01T13:21:29.821623Z"
    }
   },
   "outputs": [
    {
     "data": {
      "text/plain": [
       "464000.0"
      ]
     },
     "execution_count": 18,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "#옷가게 할인 받기\n",
    "def solution(price):\n",
    "    if price >= 50*10000:\n",
    "        answer = price*0.8 \n",
    "    elif price >=30*10000:\n",
    "        answer = price*0.9\n",
    "    elif price >=10*10000:\n",
    "        answer = price*0.95\n",
    "    else:\n",
    "        answer = price    \n",
    "    \n",
    "    return int(answer)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "b89768cb",
   "metadata": {},
   "outputs": [],
   "source": [
    "#아이스 아메리카노\n",
    "def solution(money):\n",
    "    answer = []\n",
    "    answer.append(int(money//5500))\n",
    "    answer.append(int(money%5500))\n",
    "    return answer"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "5908d36b",
   "metadata": {},
   "outputs": [],
   "source": [
    "#나이 출력\n",
    "def solution(age):\n",
    "    answer = 2022-age+1\n",
    "    return answer"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "c70b1cb0",
   "metadata": {},
   "outputs": [],
   "source": [
    "#배열 뒤집기\n",
    "def solution(num_list):\n",
    "    answer = []\n",
    "    for i in range(len(num_list)):\n",
    "        answer.append(num_list.pop(-1))\n",
    "    return answer"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "aa29b96d",
   "metadata": {},
   "source": [
    "### day 6"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 35,
   "id": "25b61ae9",
   "metadata": {
    "ExecuteTime": {
     "end_time": "2023-08-02T04:54:45.826626Z",
     "start_time": "2023-08-02T04:54:45.807186Z"
    }
   },
   "outputs": [],
   "source": [
    "#문자열 뒤집기\n",
    "def solution(my_string):\n",
    "    answer = ''\n",
    "    my_string = list(my_string)\n",
    "    my_string.reverse()\n",
    "    answer = ''.join(my_string)\n",
    "    return answer"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 37,
   "id": "15f13139",
   "metadata": {
    "ExecuteTime": {
     "end_time": "2023-08-02T04:55:55.078626Z",
     "start_time": "2023-08-02T04:55:55.066082Z"
    }
   },
   "outputs": [],
   "source": [
    "#직각 삼각형\n",
    "n = int(input())\n",
    "for i in range(1,n+1):\n",
    "    print('*'*i)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 42,
   "id": "b656b8c4",
   "metadata": {
    "ExecuteTime": {
     "end_time": "2023-08-02T05:21:44.224573Z",
     "start_time": "2023-08-02T05:21:44.195205Z"
    }
   },
   "outputs": [],
   "source": [
    "#짝수 홀수 개수\n",
    "def solution(num_list):\n",
    "    answer = []\n",
    "    even = 0\n",
    "    odd = 0\n",
    "    for i in num_list:\n",
    "        if i%2 == 0:\n",
    "            even += 1\n",
    "        else:\n",
    "            odd += 1\n",
    "\n",
    "    answer.append(even)\n",
    "    answer.append(odd)\n",
    "    return answer"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "a54ae205",
   "metadata": {
    "ExecuteTime": {
     "end_time": "2023-08-02T05:21:04.680626Z",
     "start_time": "2023-08-02T05:21:04.657676Z"
    }
   },
   "outputs": [],
   "source": [
    "#문자 반복 출력하기\n",
    "def solution(my_string, n):\n",
    "    answer = ''\n",
    "    \n",
    "    for i in my_string:\n",
    "        answer += i*n\n",
    "    \n",
    "    return answer"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "74efdb22",
   "metadata": {},
   "source": [
    "### meet"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "405f56ca",
   "metadata": {},
   "outputs": [],
   "source": [
    "def solution(price, money, count):\n",
    "    answer = 0\n",
    "    total = 0\n",
    "    \n",
    "    for i in range(1,count+1):\n",
    "        total += price*i\n",
    "    answer = money-total\n",
    "    \n",
    "    if answer >= 0:\n",
    "        answer = 0\n",
    "    \n",
    "    return abs(answer)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 17,
   "id": "92928b46",
   "metadata": {
    "ExecuteTime": {
     "end_time": "2023-08-03T05:24:42.341868Z",
     "start_time": "2023-08-03T05:24:42.323868Z"
    }
   },
   "outputs": [
    {
     "data": {
      "text/plain": [
       "30.0"
      ]
     },
     "execution_count": 17,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "#(3+12)*4/2\n",
    "\n",
    "price = 3\n",
    "count=4\n",
    "\n",
    "(price+(price*count))*count/2\n"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "5a32632a",
   "metadata": {},
   "outputs": [],
   "source": []
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "61beaf94",
   "metadata": {},
   "outputs": [],
   "source": []
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3 (ipykernel)",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.11.4"
  },
  "toc": {
   "base_numbering": 1,
   "nav_menu": {},
   "number_sections": true,
   "sideBar": true,
   "skip_h1_title": false,
   "title_cell": "Table of Contents",
   "title_sidebar": "Contents",
   "toc_cell": false,
   "toc_position": {},
   "toc_section_display": true,
   "toc_window_display": false
  }
 },
 "nbformat": 4,
 "nbformat_minor": 5
}
