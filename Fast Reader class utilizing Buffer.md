**// Fast Reader class utilizing BufferedReader and StringTokenizer**



class FastReader {

&#x20;   BufferedReader br;

&#x20;   StringTokenizer st;



&#x20;   public FastReader() {

&#x20;       br = new BufferedReader(new InputStreamReader(System.in));

&#x20;   }



&#x20;   String next() {

&#x20;       while (st == null || !st.hasMoreElements()) {

&#x20;           try {

&#x20;               st = new StringTokenizer(br.readLine());

&#x20;           } catch (IOException e) {

&#x20;               e.printStackTrace();

&#x20;           }

&#x20;       }

&#x20;       return st.nextToken();

&#x20;   }



&#x20;   int nextInt() { return Integer.parseInt(next()); }

&#x20;   long nextLong() { return Long.parseLong(next()); }

}



