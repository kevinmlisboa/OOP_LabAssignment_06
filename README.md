# 𝙻𝚊𝚋-𝙰𝚜𝚜𝚒𝚐𝚗𝚖𝚎𝚗𝚝-𝟼

## 𝚄𝙼𝙻 𝙳𝚒𝚊𝚐𝚛𝚊𝚖 
![Blank diagram (1)](https://github.com/kevinmlisboa/OOP_LabAssignment_06/assets/133233113/47523351-89ce-4895-8adc-a724e8124e22)


## 𝙸𝚗𝚜𝚝𝚛𝚞𝚌𝚝𝚒𝚘𝚗𝚜 :

𝙸𝚖𝚙𝚛𝚘𝚟𝚎 𝚝𝚑𝚎 𝚏𝚘𝚕𝚕𝚘𝚠𝚒𝚗𝚐 𝚌𝚘𝚍𝚎𝚜 𝚝𝚘 𝚒𝚖𝚙𝚕𝚎𝚖𝚎𝚗𝚝 𝚂𝙾𝙻𝙸𝙳 𝚙𝚛𝚒𝚗𝚌𝚒𝚙𝚕𝚎𝚜 𝚒𝚗 𝙾𝙾𝙿.


public interface Order {

  void calculateTotal(double price, int quantity);

  void placeOrder(String customerName, String address);

  void generateInvoice(String fileName);

  void sendEmailNotification(String email);
}

public class OrderAction implements Order {

  @Override
  public void calculateTotal(double price, int quantity) {
    double total = price * quantity;
    System.out.println("Order total: $" + total);
  }

  @Override
  public void placeOrder(String customerName, String address) {
    // Simulate placing order in a system
    System.out.println("Order placed for " + customerName + " at " + address);
  }

  @Override
  public void generateInvoice(String fileName) {
    // Simulate generating invoice file
    System.out.println("Invoice generated: " + fileName);
  }

  @Override
  public void sendEmailNotification(String email) {
    // Simulate sending email notification
    System.out.println("Email notification sent to: " + email);
  }
}

public class OrderTest {

  public static void main(String[] args) {
    Order order = new OrderAction();
    order.calculateTotal(10.0, 2);
    order.placeOrder("John Doe", "123 Main St");

    // These methods might not be needed for all orders
    order.generateInvoice("order_123.pdf");
    order.sendEmailNotification("johndoe@example.com");
  }
}


