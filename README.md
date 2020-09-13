# C-HackerRank

### Box It!
```
#include<bits/stdc++.h>

using namespace std;
//Implement the class Box
class Box{
    private:
    int l,b,h;
    public:
    Box()
    {
        l=0;
        b=0;
        h=0;
    }
    Box(int le, int br, int he)
    {
        l=le;
        b=br;
        h=he;
    }
    Box(const Box& B)
    {
        l=B.l;
        b=B.b;
        h=B.h;
    }
    int getLength()
    {
        return l;
    }
    int getBreadth()
    {
        return b;
    }
    int getHeight()
    {
        return h;
    }
    long long CalculateVolume()
    {
        return (long long)l*b*h;
    }
    friend bool operator<(Box& A, Box& B) 
    {
        //Box box;
        if (A.l<B.l || A.l ==B.l && A.b<B.b || A.l ==B.l && A.b==B.b && A.h==B.h)
        {
            return true;
        }
        else 
        {
            return false;
        }
    }
    friend ostream& operator<<(ostream& output, Box& B)
    {
        output<<B.l<<" "<<B.b<<" "<<B.h;
        return output;
    }
};

```
