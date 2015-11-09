# oopAssignment
#include<iostream>
#include<conio.h>
using namespace  std;
class  OrderDetail
{
public:

    OrderDetail()
    {
        _Id=0;
        qnty=0;

    }
     OrderDetail(int I,int q)
    {
        setId(I);
        setqnty(q);

    }
    void setId(int I)
    {
        _Id=I;
    }
    int getId()
    {
      return _Id;
    }
    void setqnty(int Q)
    {
        qnty=Q;
    }
    int getqnty()
    {
      return qnty;
    }
    void display()
    {
        cout<<" Order Id  "<<_Id<<"   quantity  "<<qnty<<endl;
        cout<<"_______________________________________________"<<endl;
    }


private:
    int _Id;
    int qnty;
};
class  Item:OrderDetail
{
public:
    Item()
    {


    }
     Item(int It,int P,string t,string N,string Ds,string up ,string Cr,int I,int Q )
    {
        set_ItemId(It);
        setPrice(P);
        setname(N);
        setupdt(up);
        setdes(Ds);
        setcret(Cr);
        setId(I);
        setqnty(Q);
        settype(t);

    }
    void setcret(string crt)
    {
        cret=crt;
    }
    string getcret()
    {
      return cret;
    }
    void setupdt(string up)
    {
        updt=up;
    }
    string getupdt()
    {
      return updt;
    }
    void setdes(string Dees)
    {
        des=Dees;
    }
    string getdes()
    {
      return des;
    }
    void settype(string Typ)
    {
        type=Typ;
    }
    string gettype()
    {
      return type;
    }
    void setname(string nme)
    {
        name=nme;
    }
    string getname()
    {
      return name;
    }
    void set_ItemId(int ItmId)
    {
        _ItemId=ItmId;
    }
    int getItemId()
    {
      return _ItemId;
    }
    void setPrice(int Prce)
    {
        Price=Prce;
    }
    int getPrice()
                {
                  return Price;
                }
    void display()
                {
            cout<<"\n_______________________________________________"<<endl;
               cout<<"USER ID :                        "<<getId()
                <<"\n ITEM ID                          "<<_ItemId
                <<"\nPrice                             "<<Price
                <<"\n Name                             "<<name
                <<"\nDescription                       "<<des
                <<"\nUpdate                            "<<updt
                <<"\nCreate                            "<<cret
                <<" \nTYPE                             "<<type
                <<endl;
                }
private:
    int _ItemId;
    int Price;
    string name,des,updt,cret,type;
};
class Order:OrderDetail
{
public:
    Order( string  s,string d,string dt,string pt,string pf,string un ,int I,int q)
    {
        setId(I);
        setqnty(q);
        setstatus(s);
        setdeliveryTo(d);
        setdeliveryTime(dt);
        setPickupTime(pt);
        setPickupForm(pf);
        setUsername(un);

    }
    void setstatus(string stat)
    {
        status=stat;
    }
    string getstatus()
    {
      return status;
    }
    void setUsername(string Usrnme)
    {
        Username=Usrnme;
    }
    string getUsername()
    {
      return Username;
    }

    void setdeliveryTo(string dlvryTo)
    {
        deliveryTo=dlvryTo;
    }
    string getdeliveryTo()
    {
      return deliveryTo;
    }
    void setdeliveryTime(string dlvyTme)
    {
        deliveryTime=dlvyTme;
    }
    string getdeliveryTime()
    {
      return deliveryTime;
    }
    void setPickupTime(string PckupTme)
    {
        PickupTime=PckupTme;
    }
    string getPickupTime()
    {
      return PickupTime;
    }
    void setPickupForm(string PckupFrm)
    {
        PickupForm=PckupFrm;
    }
    string getPickupForm()
    {
      return PickupForm;
    }
    void display()
                {
    cout<<"_______________________________________________"<<endl;
                   cout<<endl
                   <<"\nUSER ID                       "<<getId()
                   <<"\nUSER NAME                     "<<Username
                   <<"\nQuantity                      "<<getqnty()
                   <<"\nStatus                        "<<status
                   <<"\nDelivery TO                   "<<deliveryTo
                   <<"\nDElivery time                 "<<deliveryTime
                   <<"\nPickup Time                   "<<PickupTime
                   <<"\nPICK UP FORM                  "<<PickupForm
                   ;
                }
private:
  string  status,deliveryTo,deliveryTime,PickupTime,PickupForm,Username;
};
int main()
{

    OrderDetail oo(11,1);
    oo.setId(11);
    oo.setqnty(232);

    oo.display();
    Order OD("ddd","Mr XYZ","23rd December","6:00 pm","Parcel","XYZ PARCEl",11,232);
    OD.setstatus("Active");
    OD.display();
    Item d(11,232,"Type","...",".....","....","....",11,232);
    d.setdes("product is available");
    d.display();
    getch();
    return 0;
}
