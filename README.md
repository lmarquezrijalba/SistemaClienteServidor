# SistemaClienteServidor
public class ServerRMI extends unicastRemonteObject implements RMI {
public serverRMI ()throws RemoteException {
super(); lo qque hace es llamr el constructor a la  clase
}

public static void  main (string [] args){
 try{
 registry  registro=LocateRegistry.createRegistry (7777);
 registry.rebind("RemotoRMI", new serverRMI ()); // mantiene el servidor en escucha 
 system.out.println ("servidor Activo");
 
 }catch (RemoteException ex){
 system.out.println( ex.getMessage());
 }


}

