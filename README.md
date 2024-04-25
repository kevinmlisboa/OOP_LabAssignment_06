# 𝙻𝚊𝚋-𝙰𝚜𝚜𝚒𝚐𝚗𝚖𝚎𝚗𝚝-𝟼

## 𝚄𝙼𝙻 𝙳𝚒𝚊𝚐𝚛𝚊𝚖 
![Blank diagram (1)](https://github.com/kevinmlisboa/OOP_LabAssignment_06/assets/133233113/47523351-89ce-4895-8adc-a724e8124e22)


## 𝙸𝚗𝚜𝚝𝚛𝚞𝚌𝚝𝚒𝚘𝚗𝚜 :

𝙸𝚖𝚙𝚛𝚘𝚟𝚎 𝚝𝚑𝚎 𝚏𝚘𝚕𝚕𝚘𝚠𝚒𝚗𝚐 𝚌𝚘𝚍𝚎𝚜 𝚝𝚘 𝚒𝚖𝚙𝚕𝚎𝚖𝚎𝚗𝚝 𝚂𝙾𝙻𝙸𝙳 𝚙𝚛𝚒𝚗𝚌𝚒𝚙𝚕𝚎𝚜 𝚒𝚗 𝙾𝙾𝙿.


public interface Order {<br> 

  void calculateTotal(double price, int quantity);<br> 

  void placeOrder(String customerName, String address);<br> 

  void generateInvoice(String fileName);<br> 

  void sendEmailNotification(String email);<br> 
}<br> 

public class OrderAction implements Order {<br> 

  @Override<br> 
  public void calculateTotal(double price, int quantity) {<br> 
    double total = price * quantity;<br> 
    System.out.println("Order total: $" + total);<br> 
  }<br> 

  @Override
  public void placeOrder(String customerName, String address) {<br> 
    // Simulate placing order in a system<br> 
    System.out.println("Order placed for " + customerName + " at " + address);<br> 
  }<br> 

  @Override
  public void generateInvoice(String fileName) {<br> 
    // Simulate generating invoice file<br> 
    System.out.println("Invoice generated: " + fileName);<br> 
  }<br> 

  @Override<br> 
  public void sendEmailNotification(String email) {<br> 
    // Simulate sending email notification <br> 
    System.out.println("Email notification sent to: " + email);<br> 
  }<br> 
}<br> 

public class OrderTest { <br> 

  public static void main(String[] args) { <br>  
    Order order = new OrderAction(); <br>  
    order.calculateTotal(10.0, 2); <br> 
    order.placeOrder("John Doe", "123 Main St"); <br> 

    // These methods might not be needed for all orders<br> 
    order.generateInvoice("order_123.pdf");<br> 
    order.sendEmailNotification("johndoe@example.com");<br> 
  }<br> 
}<br> 


