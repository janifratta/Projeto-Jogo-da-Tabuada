# Projeto-Jogo-da-Tabuada
Game criado para entrega no final de semestre na FATENP (Outubro/2016)

>>PLAYER

public class PlayerShooter : MonoBehaviour {

    Rigidbody2D rb;
    Animator anim;

    void Start () {
        rb = GetComponent<Rigidbody2D>();
        anim = GetComponent<Animator>();
	}
    void OnMouseUp()
    {
        //Debug.Log("Clicado!");
        Atirar();
    }
    //modificar o codigo para quando der um clique no alvo o mesmo se revela (animação) 
    public virtual void Atirar() {
        anim.SetBool("girar", true);
	}
}

>>INICIARGAME

public class InicioJogodaTabuada : MonoBehaviour {

	void Update () {

        if(Input.GetMouseButtonDown(0)){
            Application.LoadLevel("gameJDT");
        }
	}
}
