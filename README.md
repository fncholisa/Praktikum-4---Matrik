# Praktikum-4---Matrik
public class Praktikum4 {
    private int[][] x,  y,  hasilJum;
    private double[][] hasilKal;

    public void setMatrikX(int[][] x) {
        this.x = x;
        x = null;
    }

    public int[][] getMatrikX() {
        return x;
    }

    public void setMatrikY(int[][] y) {
        this.y = y;
        y = null;
    }

    public int[][] getMatrikY() {
        return y;
    }

    public void setJumlah(int[][] x, int[][] y) {
        hasilJum = new int[x.length][x[0].length];
        int i, j;
        for (i = 0; i < x.length; i++) {
            for (j = 0; j < x[i].length; j++) {
                hasilJum[i][j] = x[i][j] + y[i][j];
            }
        }
        x = null;
        y = null;
    }

    public int[][] getJumlah() {
        return hasilJum;
    }

    public void setKali(int[][] data, double x) {
        hasilKal = new double[data.length][data[0].length];
        int i, j;
        for (i = 0; i < data.length; i++) {
            for (j = 0; j < data[i].length; j++) {
                hasilKal[i][j] = x * data[i][j];
            }
        }
        data = null;
    }

    public double[][] getKali() {
        return hasilKal;
    }

    public void tampil(String x) {
        System.out.println(x);
        x = null;
    }

    public void tampil(double data[][]) {
        int i, j;
        for (i = 0; i < data.length; i++) {
            for (j = 0; j < data[i].length; j++) {
                System.out.print(data[i][j] + "   ");
            }
            System.out.println();
        }
        data = null;
    }

    public void tampil(int data[][]) {
        int i, j;
        for (i = 0; i < data.length; i++) {
            for (j = 0; j < data[i].length; j++) {
                System.out.print(data[i][j] + "   ");
            }
            System.out.println();
        }
        data = null;
    }

    public void hapus() {
        x = null;
        y =null;
        hasilJum = null;
        hasilKal = null;
    }
}





public class App {
    public static void main(String[] args) {
        Praktikum4 b =new Praktikum4();
        int[][]x={{1,2},{3,5},{6,7}};
        int[][]y={{8,9},{10,11},{12,13}};
        double pengali=0.5;
        b.tampil("Data Matrik A : ");
        b.setMatrikX(x);
        b.tampil(b.getMatrikX());
        b.tampil("Data Matrik B : ");
        b.setMatrikY(y);
        b.tampil(b.getMatrikY());
        b.tampil("Data Matrik C : ");
        b.setJumlah(x, y);
        b.tampil(b.getJumlah());
        b.tampil("Data Matrik B x "+pengali+" : ");
        b.setKali(b.getMatrikY(), pengali);
        b.tampil(b.getKali());

        b.hapus();
        x=null;
        y=null;
        b=null;
    }
    
        
}



