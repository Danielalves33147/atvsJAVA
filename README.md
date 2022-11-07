 #atvsJAVA
Atividades de POO em Java, no 3º semestre 2022

package danielalves;

import javax.swing.JOptionPane;

public class PrincipalComputador {
    public static void main(String[] args){
        
        Computador comp = new Computador();
        String sc;
        
        sc = JOptionPane.showInputDialog(null,"Informe a marca: ");
        comp.setMarca(sc);
        
        sc = JOptionPane.showInputDialog(null,"Informe a cor: ");
        comp.setCor(sc);
        
        sc = JOptionPane.showInputDialog(null,"Informe o modelo: ");
        comp.setModelo(sc);
        
        sc = JOptionPane.showInputDialog(null,"Informe o Nº de Serie: ");
        comp.setSerie_num(Integer.parseInt(sc));
        
        sc = JOptionPane.showInputDialog(null,"Informe o Preco: ");
        comp.setPreco(Float.parseFloat(sc));
        
        
        comp.calculaValor();
        if (comp.alteraValor(20) == 1){
            JOptionPane.showMessageDialog(null,"Valor Alterado!");
        }else{
            JOptionPane.showMessageDialog(null,"Valor NÃO Alterado!");
        }
        comp.imprimir();
    }
}
