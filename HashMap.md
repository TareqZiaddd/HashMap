# HashMap

ي Java:

إحصاء الكلمات:
مشكلة: كتابة برنامج يقوم بعداد عدد مرات ظهور كل كلمة في نص معين.
الحلاحتمالات:

java
Copy code
import java.util.HashMap;

public HashMap<String, Integer> countWords(String text) {
    HashMap<String, Integer> wordCount = new HashMap<>();
    String[] words = text.split(" ");
    for (String word : words) {
        wordCount.put(word, wordCount.getOrDefault(word, 0) + 1);
    }
    return wordCount;
}
البحث عن العنصر:
مشكلة: كتابة دالة تبحث عن وجود عنصر معين في هاش ماب.
الحلاحتمالات:

java
Copy code
public boolean searchElement(HashMap<String, Integer> map, String key) {
    return map.containsKey(key);
}
إزالة العنصر:
مشكلة: كتابة دالة لإزالة عنصر معين من هاش ماب.
الحلاحتمالات:

java
Copy code
public void removeElement(HashMap<String, Integer> map, String key) {
    map.remove(key);
}
الحصول على مفاتيح الهاش ماب:
مشكلة: كتابة دالة لاسترجاع جميع المفاتيح الموجودة في هاش ماب.
الحلاحتمالات:

java
Copy code
public Set<String> getKeys(HashMap<String, Integer> map) {
    return map.keySet();
}
الحصول على القيم من الهاش ماب:
مشكلة: كتابة دالة لاسترجاع جميع القيم الموجودة في هاش ماب.
الحلاحتمالات:

java
Copy code
public Collection<Integer> getValues(HashMap<String, Integer> map) {
    return map.values();
هذه مشكلات سهلة تستخدم هاش ماب في Java. يمكنك استخدام هذه الأمثلة لتعلم كيفية العمل مع هاش ماب وكيفية حل مشكلات مختلفة باستخدامه.


***************************************************************************************************
************************************************************************************************************
******************************************************************************************************************
/*{Ahmad= 1
basel = 2
Amjad = 3
}
target = a
output//
{Amjad,Ahmad}
// إيجاد جميع القيم في الهاش ماب التي تبدأ بحرف معين باستخدام ميثود
 * 
 * 
 * 
 * */
 
public static List<String> findValuesStartingWith(HashMap<String, Integer> hashMap, char target) {





List <String> list1 = new ArrayList <>();
for (String key:hashMap.keySet()) {
	if (key.charAt(0)==target) {
		list1.add(key);
	}
}
return list1;
	
	
}
*********************************************************
هات نفس ال سؤال بس رجع ال 
value

/*{Ahmad= 1
basel = 2
Amjad = 3
}
target = 1
output//
{1}
/ اذا التارغيت اللي طلبتو منك موجود رجعلي اياه 
 * 
 * 
 * 
 * */
 
public static List<Integer> findValuesStartingWith(HashMap<String, Integer> hashMap,Integer target) {
List <Integer> list1 = new ArrayList <>();
for (String key:hashMap.keySet()) {
	int value = hashMap.get(key);

	if (value ==target) {
list1.add(value);
}
}
return list1;
	
	
}

------------------------------------------------------------
نفس الكود بنعطيك التاريغيت اللي هو 
value
وبترجعلنا 
ال key
تاع التارغيت 



/*{Ahmad= 1
basel = 2
Amjad = 3
}
target = 1
output//
Ahmad
// إيجاد جميع القيم في الهاش ماب التي تبدأ بحرف معين باستخدام ميثود
 * 
 * 
 * 
 * */
 
public static List<String> findValuesStartingWith(HashMap<String, Integer> hashMap,Integer target) {
List <String> list1 = new ArrayList <>();
for (String key:hashMap.keySet()) {
	int value = hashMap.get(key);

	if (value ==target) {
list1.add(key);
}
}
return list1;
	
	
}
---------------------------------------------------


# append
list1 = [1, 2, 3]
list1.append(4)
print(list1)
# [1, 2, 3, 4]

# add
list2 = [1, 2, 3]
list2.add(4)
print(list2)
# [1, 2, 3, 4]

# add to the beginning
list3 = [1, 2, 3]
list3.add(0, 4)
print(list3)
# [4, 1, 2, 3]

--------------------------------------------------------------------------------

كود لتحديث عمر شخص معين 
حيث هذا الشخص اسمه وعمره موجودين في هاش ماب 

	
/*{Ahmad= 1
basel = 2
Amjad = 3
}
newAge = 100
output//
{b=2, amjad=3, ahmad=100}
// تحديث عمر شخص ما 
 * 
 * 
 * 
 * */
    public static void updateAge(HashMap<String, Integer> people, String name, int newAge) {
        if (people.containsKey(name)) {
            people.put(name, newAge);
        }


    }

-----------------------------------------------------------------------
هات نفس الكود ولكن مع طباعة الكود القديم وطبعاة الهاش ماب 


	  public static void updateAge(HashMap<String, Integer> map, String name, int newAge) {




	        if (map.keySet().contains(name))	            // تحديث العمر
	            map.put(name, newAge);

	            // طباعة الهاش ماب بعد التحديث
	            System.out.println(map);

	            // طباعة العمر القديم
	            System.out.println("oldAge = " + map.get(name));
	        }
	    }
******************************************************************************************
profile picture
لماذا وضعنا هنا map.ketSet.contains ولم نضع مباشرة map.contains? 	  public static void updateAge(HashMap<String, Integer> map, String name, int newAge) {
	        if (map.keySet().contains(name)) {
	            // تحديث العمر
	            map.put(name, newAge);

	            // طباعة الهاش ماب بعد التحديث
	            System.out.println(map);

	            // طباعة العمر القديم
	            System.out.println("oldAge = " + map.get(name));
	        }
	    }
View other drafts

*********************************************************************************************************************************

نضع map.keySet().contains() بدلاً من map.contains() لأن map.contains() تتحقق من وجود العنصر في الهاش ماب، بغض النظر عن نوع العنصر. أما map.keySet().contains() فتتحقق من وجود العنصر في مجموعة المفاتيح الخاصة بالهاش ماب، والتي تتكون فقط من المفاتيح.

في هذا المثال، نريد التحقق من وجود اسم الشخص في مجموعة المفاتيح الخاصة بالهاش ماب. لذلك، نستخدم map.keySet().contains().

فيما يلي مثال على الفرق بين map.contains() و map.keySet().contains():

Java
HashMap<String, Integer> map = new HashMap<>();
map.put("John Doe", 30);
map.put("Jane Doe", 25);

System.out.println(map.contains("John Doe")); // true
System.out.println(map.keySet().contains("John Doe")); // true

System.out.println(map.contains(30)); // false
System.out.println(map.keySet().contains(30)); // false
Use code with caution. Learn more
سيؤدي هذا الكود إلى طباعة الإخراج التالي:

true
true
false
false
الإخراج الأول والثاني يوضحان أن map.contains() و map.keySet().contains() ترجع نفس النتيجة إذا كان العنصر موجودًا في مجموعة المفاتيح.

الإخراج الثالث والرابع يوضحان أن map.contains() سترجع نتيجة خاطئة إذا لم يكن العنصر موجودًا في مجموعة المفاتيح، ولكن كان موجودًا في الهاش ماب. أما map.keySet().contains() فسترجع نتيجة صحيحة في هذه الحالة.




********************************************************************************************************************************************************
كود بطبع المفتاح والقيمة تاعته بهذا الشكا

key = b, value = 2
key = amjad, value = 3
key = ahmad, value = 1


	public static void printKeysValues(HashMap<String, Integer> map) {
	    for (String key : map.keySet()) {
	        System.out.println("key = " + key + ", value = " + map.get(key));
	    }
	}
------------------------------------------------------------------------------------------------------------------------------------------




	//input String sentence = "This is a long sentence.";
	//output  longestWord: sentence
	public static String processSentence(String sentence) {
		
		int lengthLongestWord = 0 ;
		String longestWord= "";
		String words [] = sentence.split(" "); 
	//[this,is,a,long,sentence]
		for (String word:words) {
			if(word.length()>lengthLongestWord) {
				lengthLongestWord=word.length();
				longestWord=word;
			}
		
		}
		return longestWord;
	}

---------------------------------------------------------------------------------------------------------------------
ChatGPT
بالطبع، إليك كود بسيط في Java لطباعة جميع المفاتيح والقيم في هاش ماب:
java
Copy code
import java.util.HashMap;
import java.util.Map;
public class PrintHashMap {
    public static void main(String[] args) {
        // إنشاء هاش ماب وإضافة بعض القيم
        Map<String, Integer> hashMap = new HashMap<>();
        hashMap.put("John", 25);
        hashMap.put("Alice", 30);
        hashMap.put("Bob", 28);
        // طباعة المفاتيح والقيم في الهاش ماب
        System.out.println("المفاتيح والقيم في الهاش ماب:");
        for (Map.Entry<String, Integer> entry : hashMap.entrySet()) {
            System.out.println("المفتاح: " + entry.getKey() + ", القيمة: " + entry.getValue());
        }
    }
}
-----------------------------------------------------------------------------------
عد الكاركترات اللي بالسترينغ
	  String str = "The quick brown fox jumps over the lazy dog.";

//OUTPUT
{T=1,  =8, a=1, b=1, c=1, d=1, e=3, f=1, g=1, h=2, i=1, j=1, k=1, l=1, m=1, n=1, .=1, o=4, p=1, q=1, r=2, s=1, t=1, u=2, v=1, w=1, x=1, y=1, z=1}



	public static Map<Character,Integer> countCharacters (String str){
		Map <Character,Integer> map = new HashMap <>();
	char [] ch = str.toCharArray();
	//ch= {t h e q u i c k  b r o w n f o x}
for (Character charr:ch) {
	map.put(charr, map.getOrDefault(charr,0)+1);
}
return map;
	}

-------------------------------------------------------------------------------------------
Word frequencies: {Write=2, code=2, to=2, find=1, the=1, longest=1, word=1, in=1, a=1, sentence=1, test=1, program=1}
Most frequent word: Write (Frequency: 2)
Least frequent word: in, a, sentence, test, program (Frequency: 1)

برنامج برجع اصغر كلمة واكبر كلمة في السترينغ

import java.util.HashMap;
import java.util.Map;
public class Main {
    public static void main(String[] args) {
        String sentence = "Write a code to find the longest word in a sentence. Write code to test the program.";
        String result = processSentence(sentence);
        System.out.println("Word with most occurrences: " + result);
    }
    public static String processSentence(String sentence) {
        String[] words = sentence.split("\\s+");
        String mostFrequentWord = "";
        String leastFrequentWord = "";
        int maxFrequency = 0;
        int minFrequency = Integer.MAX_VALUE;
        Map<String, Integer> wordFrequencyMap = new HashMap<>();
        for (String word : words) {
            int frequency = wordFrequencyMap.getOrDefault(word, 0) + 1;
            wordFrequencyMap.put(word, frequency);
            if (frequency > maxFrequency) {
                maxFrequency = frequency;
                mostFrequentWord = word;
            }
            if (frequency < minFrequency) {
                minFrequency = frequency;
                leastFrequentWord = word;
            }
        }
        System.out.println("Word frequencies: " + wordFrequencyMap);
        System.out.println("Most frequent word: " + mostFrequentWord + " (Frequency: " + maxFrequency + ")");
        System.out.println("Least frequent word: " + leastFrequentWord + " (Frequency: " + minFrequency + ")");
        return mostFrequentWord;
    }
}

















map.entrySet()
هات الحل نفسه ولكن 
map.values()
map.keySet()

------------------------------------------------------------------------------
شوف سترينغ عبارة عن جملة يعني مجموعة كلمات واطبع اطول كلمة فيها مع ذكر كم طولها
واطبع اصغر كلمة فيها مع ذكر طول اصغر كلمة


public static void countCharacters (String s){
int maxLength = 0;
int minLength=0;
String maxWord="";
String minWord="";
String [] words =s.split(" ");
for (String word:words) {
	if (word.length()>maxLength) {
		maxLength=word.length();
		maxWord=word;
		if(word.length()<minLength) {
			minLength = word.length();
			minWord=word;		
					}
	}
}
		System.out.println("minLength="+minLength+"minWord = "+minWord);
		System.out.println("maxLength="+maxLength+"maxWord = "+maxWord);
		

	}

--------------------------------------------------------------------------------
زيد عالكود كمان انك تقدر ترجع كل كلمة كم مرة تكررت

public static void countCharacters (String s){
int maxLength = 0;
int minLength=0;
String maxWord="";
String minWord="";
String [] words =s.split(" ");
for (String word:words) {
	if (word.length()>maxLength) {
		maxLength=word.length();
		maxWord=word;
		if(word.length()<minLength) {
			minLength = word.length();
			minWord=word;		
					}
	}
}
		System.out.println("minLength="+minLength+"minWord = "+minWord);
		System.out.println("maxLength="+maxLength+"maxWord = "+maxWord);
		

	}
---------------------------------------------------------------
زيد عالكود كمان انك تقدر ترجع كل كلمة كم مرة تكررت

public static void countWords(String s){
int maxLength = 0;
int minLength=0;
String maxWord="";
String minWord="";
Map<String,Integer>wordMap=new HashMap <>();
String [] words =s.split(" ");
for (String word:words) {
	wordMap.put(word, wordMap.getOrDefault(word, 0)+1);

	if (word.length()>maxLength) {
		maxLength=word.length();
		maxWord=word;
		if(word.length()<minLength) {
			minLength = word.length();
			minWord=word;		
					}
	}
}
		System.out.println("minLength="+minLength+"minWord = "+minWord);
		System.out.println("maxLength="+maxLength+"maxWord = "+maxWord);
		System.out.println(wordMap);

	}

---------------------------------------------------------------------------------------------------



رجعلي كل القيم اللي بهاش ماب وبكونو اكبر من 1
    ("ahmad", 1) ("basel", 2) ("amjad", 3);
targetValue=1;
//output
[2, 3]


public static List<Integer> add (HashMap <String,Integer>map,int targetValue){


	List<Integer>list = new ArrayList<>();
	for (String key:map.keySet()) {
		if(map.get(key)>targetValue) {
			list.add(map.get(key));
		}
	}
	return list;
}
---------------------------------------------------------------------------
رجعلي كل االمفاتيح اللي من نوع سترينغ اللي بتبلش بحرف معين

inputs:
map=
ahmad"= 1
"basel"= 2
"amjad"= 3
target='a'

//output:
[3, 1]



public static List<Integer> findValuesByPrefix(HashMap<String, Integer> hashMap, char target) {
        List<Integer> values = new ArrayList<>();
        for (String key : hashMap.keySet()) {
            if (key.startsWith(String.valueOf(target))) {
                values.add(hashMap.get(key));
            }
        }
        return values;
    }
----------------------------------------------------------------------------------------
حل اخر اسهل
public class Main {
    public static List<String> findValuesByPrefix(HashMap<String, Integer> hashMap, char target) {
        List<String>values = new ArrayList<>();
        for (String word : hashMap.keySet()) {
           if(word.charAt(0)==target) {
        	   values.add(word);
            }
        }
        return values;
    }

-----------------------------------------------------------------------------------------------
ال
keys
من نوع سترينغ
اللي بينتهو ب حرف اخير
رجع منهم 
ال keys 
تاعونهم
input
inputs:
map=
ahmad"= 1
"basel"= 2
"amjad"= 3

target='d'

//output
[amjad, ahmad]

public class FindValuesByPrefix {

    public static List<String> findValuesByPrefix(HashMap<String, Integer> hashMap, char target) {
        List<String> values = new ArrayList<>();
        for (String word : hashMap.keySet()) {
            if (word.charAt(word.length() - 1) == target) {
                values.add(word);
            }
        }
        return values;
    }

























-------------------------------------------------------------------------
Two Sum
Example 1:

Input: nums = [2,7,11,15], target = 9
Output: [0,1]
Explanation: Because nums[0] + nums[1] == 9, we return [0, 1].

Example 2:

Input: nums = [3,2,4], target = 6
Output: [1,2]


Example 3:

Input: nums = [3,3], target = 6
Output: [0,1]


    public int[] twoSum(int[] nums, int target) {
        int[] arr = new int[2];
        HashMap<Integer, Integer> map = new HashMap<>();

        for (int i = 0; i < nums.length; i++) {
            int number = nums[i];
            if (map.containsKey(number)) {
             return new int[]{map.get(number), i};
            } else {
                map.put(target - number, i);
            }
        }

        return new int[]{-1, -1};
    }
---------------------------------------------------------------------------------------------------
roman to integer
--------------------------------------------------------------------------------------------------------------------------

Symbol       Value
I             1
V             5
X             10
L             50
C             100
D             500
M             1000



Example 1:

Input: s = "III"
Output: 3
Explanation: III = 3.
Example 2:

Input: s = "LVIII"
Output: 58
Explanation: L = 50, V= 5, III = 3.
Example 3:

Input: s = "MCMXCIV"
Output: 1994
Explanation: M = 1000, CM = 900, XC = 90 and IV = 4. 



import java.util.Map;

public class RomanToInt {
    public static int romanToInt(String s) {
        Map<String, Integer> map = Map.of("I", 1, "V", 5, "X", 10, "L", 50, "C", 100, "D", 500, "M", 1000);
        int sum = 0;
        for (int i = 0; i < s.length(); i++) {
            sum = sum + map.get(String.valueOf(s.charAt(i)));
        }
        return sum;
    }
------------------------------------------------------------------------------------------------------------------------
Roman numerals are represented by seven different symbols: I, V, X, L, C, D and M.

Symbol       Value
I             1
V             5
X             10
L             50
C             100
D             500
M             1000
For example, 2 is written as II in Roman numeral, just two one's added together. 12 is written as XII, which is simply X + II. The number 27 is written as XXVII, which is XX + V + II.

Roman numerals are usually written largest to smallest from left to right. However, the numeral for four is not IIII. Instead, the number four is written as IV. Because the one is before the five we subtract it making four. The same principle applies to the number nine, which is written as IX. There are six instances where subtraction is used:

I can be placed before V (5) and X (10) to make 4 and 9. 
X can be placed before L (50) and C (100) to make 40 and 90. 
C can be placed before D (500) and M (1000) to make 400 and 900.
Given an integer, convert it to a roman numeral.

 

Example 1:

Input: num = 3
Output: "III"
Explanation: 3 is represented as 3 ones.
Example 2:

Input: num = 58
Output: "LVIII"
Explanation: L = 50, V = 5, III = 3.
Example 3:

Input: num = 1994
Output: "MCMXCIV"
Explanation: M = 1000, CM = 900, XC = 90 and IV = 4.








import java.util.HashMap;

public class Solution {
    public String intToRoman(int num) {
        int[] hrr = {1000, 900, 500, 400, 100, 90, 50, 40, 10, 9, 5, 4, 1};
        HashMap<Integer, String> map = new HashMap<Integer, String>();
        map.put(1000, "M");
        map.put(900, "CM");
        map.put(500, "D");
        map.put(400, "CD");
        map.put(100, "C");
        map.put(90, "XC");
        map.put(50, "L");
        map.put(40, "XL");
        map.put(10, "X");
        map.put(9, "IX");
        map.put(5, "V");
        map.put(4, "IV");
        map.put(1, "I");
        
        StringBuilder sb = new StringBuilder();
        int i = 0;
        while (num > 0) {
            if (num >= hrr[i]) {
                num = num - hrr[i];
                sb.append(map.get(hrr[i]));
            } else {
                i++;
            }
        }
        return sb.toString();
    }
}

-------------------------------------------------------
Example 1:

Input: num = 3
Output: "III"
Explanation: 3 is represented as 3 ones.
Example 2:

Input: num = 58
Output: "LVIII"
Explanation: L = 50, V = 5, III = 3.
Example 3:

Input: num = 1994
Output: "MCMXCIV"
Explanation: M = 1000, CM = 900, XC =

class Solution {
    public String intToRoman(int num) {
        String roman="";
        int[] number = {1000,900,500,400,100,90,50,40,10,9,5,4,1};
        String[] s = {"M","CM","D","CD","C","XC","L","XL","X","IX","V","IV","I"};
        int i=0;
        for(i=0; i<number.length && num>=0; ++i){
            // System.out.println(i);
            while(num >= number[i]){
                
                roman += s[i];
                num -= number[i];
            }
            
        }
        return roman;
    }
}
------------------------------------------------------------------
    z = x;
        x = y;
        y = z;
