# OperatorOverloading.net<br>
<br>
using System;<br>
<br>
namespace Exercises<br>
{<br>
    class Box<br>
    {<br>
        float width;<br>
        float height;<br>
        float length;<br>
<br>
        public float Volume<br>
        {<br>
            get { return width * height * length; }<br>
        }<br>
<br>
        public Box(float width, float height, float length)<br>
        {<br>
            this.width = width;<br>
            this.height = height;<br>
            this.length = length;<br>
        }<br>
        public static float operator +(Box box1, Box box2)<br>
        {<br>
            return box1.Volume + box2.Volume;<br>
        }<br>
<br>
        public override string ToString()<br>
        {<br>
            return "box with width " + width + ",height " + height + " and length " + length;<br>
        }<br>
    }<br>
<br>
        class OperatorOverloading<br>
        {<br>
            public static void Main()<br>
            {<br>
                Box box1 = new Box(10, 20, 30);<br>
                Box box2 = new Box(25, 32, 15);<br>
<br>
                Console.WriteLine("Volume of {0} is {1}", box1, box1.Volume);<br>
                Console.WriteLine("Volume of {0} is {1}", box2, box2.Volume);<br>
                Console.WriteLine("Volume after adding boxes: {0}",box1+box2);<br>
<br>
            }<br>
        }<br>
}<br>

OUTPUT:-
![Screenshot (5)](https://user-images.githubusercontent.com/98145032/152289873-1f099e9b-944f-42eb-b463-34f8c2290bef.png)

