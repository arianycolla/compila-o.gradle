todos os projetos {
    repositórios {
      pesquise no Google()
        mavenCentral()
    }
}

val newBuildDir :  Diretório  = rootProject.layout.buildDirectory.dir( " ../../build " ).get()
rootProject.layout.buildDirectory.valor(novoBuildDir)

subprojetos {
    val newSubprojectBuildDir :  Diretório  = newBuildDir.dir(project.name)
    projeto.layout.buildDirectory.valor(novoSubprojetoBuildDir)
}
subprojetos {
    projeto.avaliaçãoDependeDe( " aplicação " )
}

tarefas.register< Excluir >( " limpar " ) {
    excluir(rootProject.layout.buildDirectory)
