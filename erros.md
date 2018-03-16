## Symfony \ Component \ HttpKernel \ Exception \ MethodNotAllowedHttpException
#### No message
If you are using post instead of get  and vice-versa

## Symfony \ Component \ HttpKernel \ Exception \ AccessDeniedHttpException
#### This action is unauthorized.
Something with policies

## ErrorException (E_ERROR)
### Cannot end a section without first starting one
Do not put two ` @endsection` inside blade file.  

## Symfony \ Component \ Debug \ Exception \ FatalThrowableError (E_RECOVERABLE_ERROR)
### Type error: Too few arguments to function App\Http\Controllers\EmpresaController::usuarioIndex(), 0 passed and exactly 1 expected
I forgot to properly set the route with `{id}` 

## Integrity
Try to usebn `$request>input` instead of  `$request>only` when requesting checkbox array

## Illuminate \ Database \ QueryException (42S22)
### SQLSTATE[42S22]: Column not found: 1054 Unknown column 'unidades_id' i
Set the foreing key  as second argument on BelongsTo method
