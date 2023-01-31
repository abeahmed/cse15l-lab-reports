# Lab Report 2: 

## 1. **Installing Visual Studio Code**: ##


   `
    import java.io.IOException;
    import java.net.URI;

    class Handler implements URLHandler {
        String outputString = "";
        String firstParameter;
        String secondParameter;
        public String handleRequest(URI url) {
            if (url.getPath().contains("/add-message")) {
                String[] URLparameters = url.getQuery().split("=");
                firstParameter = URLparameters[0];
                secondParameter = URLparameters[1];
                if (firstParameter.equals("s")) {
                    outputString = outputString + secondParameter + "\n";
                }
                return outputString;
            }
            return "invalid";
        }
    }


    class StringServer {
        public static void main(String[] args) throws IOException {
            if (args.length == 0) {
                System.out.println("Missing port number");
                return;
            }
            int port = Integer.parseInt(args[0]);

            Server.start(port, new Handler());
        }
    }
`
