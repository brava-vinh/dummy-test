node {
      stage('Checkout') {
        sh 'env'
        final scmVars = checkout(scm)
        echo env.BRANCH_NAME
        echo "Checkout"
        println scmVars.inspect()
      }

      stage('Pending') {
          sh 'env | sort'
          sh 'git rev-parse HEAD > commit'
          commit = readFile('commit').trim()
      }
}
