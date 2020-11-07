---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/resolve-azurermerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Resolve-AzureRmError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Resolve-AzureRmError.md
ms.openlocfilehash: 79c117ec7bf01c836c77fa6f6955481d7ba18a2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757245"
---
# <span data-ttu-id="ac972-101">Resolve-AzureRmError</span><span class="sxs-lookup"><span data-stu-id="ac972-101">Resolve-AzureRmError</span></span>

## <span data-ttu-id="ac972-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ac972-102">SYNOPSIS</span></span>
<span data-ttu-id="ac972-103">Visa detaljerad information om PowerShell-fel med utökad information för Azure PowerShell-fel.</span><span class="sxs-lookup"><span data-stu-id="ac972-103">Display detailed information about PowerShell errors, with extended details for Azure PowerShell errors.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac972-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ac972-104">SYNTAX</span></span>

### <span data-ttu-id="ac972-105">AnyErrorParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ac972-105">AnyErrorParameterSet (Default)</span></span>
```
Resolve-AzureRmError [[-Error] <ErrorRecord[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac972-106">LastErrorParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac972-106">LastErrorParameterSet</span></span>
```
Resolve-AzureRmError [-Last] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac972-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ac972-107">DESCRIPTION</span></span>
<span data-ttu-id="ac972-108">Matchar och visar detaljerad information om fel i den aktuella PowerShell-sessionen, inklusive var felet uppstod i skript, stack spårning och alla inre och sammansatta undantag.</span><span class="sxs-lookup"><span data-stu-id="ac972-108">Resolves and displays detailed information about errors in the current PowerShell session, including where the error occurred in script, stack trace, and all inner and aggregate exceptions.</span></span> <span data-ttu-id="ac972-109">För Azure PowerShell-fel finns mer information i fel sökning av tjänst problem, inklusive fullständig information om begäran och Server svaret som orsakade felet.</span><span class="sxs-lookup"><span data-stu-id="ac972-109">For Azure PowerShell errors provides additional detail in debugging service issues, including complete detail about the request and server response that caused the error.</span></span>

## <span data-ttu-id="ac972-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ac972-110">EXAMPLES</span></span>

### <span data-ttu-id="ac972-111">Exempel 1: Lös det senaste felet</span><span class="sxs-lookup"><span data-stu-id="ac972-111">Example 1: Resolve the Last Error</span></span>
```
PS C:\> Resolve-AzureRmError -Last

   HistoryId: 3


Message        : Run Connect-AzureRmAccount to login.
StackTrace     :    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.get_DefaultContext() in AzureRmCmdlet.cs:line 85
                    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.LogCmdletStartInvocationInfo() in AzureRmCmdlet.cs:line 269
                    at Microsoft.WindowsAzure.Commands.Utilities.Common.AzurePSCmdlet.BeginProcessing() inAzurePSCmdlet.cs:line 299
                    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.BeginProcessing() in AzureRmCmdlet.cs:line 320
                    at Microsoft.Azure.Commands.Profile.GetAzureRMSubscriptionCommand.BeginProcessing() in GetAzureRMSubscription.cs:line 49
                    at System.Management.Automation.Cmdlet.DoBeginProcessing()
                    at System.Management.Automation.CommandProcessorBase.DoBegin()
Exception      : System.Management.Automation.PSInvalidOperationException
InvocationInfo : {Get-AzureRmSubscription}
Line           : Get-AzureRmSubscription
Position       : At line:1 char:1
                 + Get-AzureRmSubscription
                 + ~~~~~~~~~~~~~~~~~~~~~~~
HistoryId      : 3
```

<span data-ttu-id="ac972-112">Få information om det senaste felet.</span><span class="sxs-lookup"><span data-stu-id="ac972-112">Get details of the last error.</span></span>

### <span data-ttu-id="ac972-113">Exempel 2: lös alla fel i sessionen</span><span class="sxs-lookup"><span data-stu-id="ac972-113">Example 2: Resolve all Errors in the Session</span></span>
```
PS C:\> Resolve-AzureRmError


   HistoryId: 8


RequestId      : b61309e8-09c9-4f0d-ba56-08a6b28c731d
Message        : Resource group 'contoso' could not be found.
ServerMessage  : ResourceGroupNotFound: Resource group 'contoso' could not be found.
                 (System.Collections.Generic.List`1[Microsoft.Rest.Azure.CloudError])
ServerResponse : {NotFound}
RequestMessage : {GET https://management.azure.com/subscriptions/00977cdb-163f-435f-9c32-39ec8ae61f4d/resourceGroups/co
                 ntoso/providers/Microsoft.Storage/storageAccounts/contoso?api-version=2016-12-01}
InvocationInfo : {Get-AzureRmStorageAccount}
Line           : Get-AzureRmStorageAccount -ResourceGroupName contoso -Name contoso
Position       : At line:1 char:1
                 + Get-AzureRmStorageAccount -ResourceGroupName contoso -Name contoso
                 + ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
StackTrace     :    at Microsoft.Azure.Management.Storage.StorageAccountsOperations.<GetPropertiesWithHttpMessagesAsync
                 >d__8.MoveNext()
                 --- End of stack trace from previous location where exception was thrown ---
                    at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
                    at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
                    at Microsoft.Azure.Management.Storage.StorageAccountsOperationsExtensions.<GetPropertiesAsync>d__7.
                 MoveNext()
                 --- End of stack trace from previous location where exception was thrown ---
                    at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
                    at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
                    at Microsoft.Azure.Management.Storage.StorageAccountsOperationsExtensions.GetProperties(IStorageAcc
                 ountsOperations operations, String resourceGroupName, String accountName)
                    at Microsoft.Azure.Commands.Management.Storage.GetAzureStorageAccountCommand.ExecuteCmdlet() in C:\
                 zd\azure-powershell\src\ResourceManager\Storage\Commands.Management.Storage\StorageAccount\GetAzureSto
                 rageAccount.cs:line 70
                    at Microsoft.WindowsAzure.Commands.Utilities.Common.AzurePSCmdlet.ProcessRecord() in
                 C:\zd\azure-powershell\src\Common\Commands.Common\AzurePSCmdlet.cs:line 642
HistoryId      : 8


   HistoryId: 5


Message        : Run Connect-AzureRmAccount to login.
StackTrace     :    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.get_DefaultContext() in C:\zd\azur
                 e-powershell\src\ResourceManager\Common\Commands.ResourceManager.Common\AzureRmCmdlet.cs:line 85
                    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.LogCmdletStartInvocationInfo() in
                 C:\zd\azure-powershell\src\ResourceManager\Common\Commands.ResourceManager.Common\AzureRmCmdlet.cs:lin
                 e 269
                    at Microsoft.WindowsAzure.Commands.Utilities.Common.AzurePSCmdlet.BeginProcessing() in
                 C:\zd\azure-powershell\src\Common\Commands.Common\AzurePSCmdlet.cs:line 299
                    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.BeginProcessing() in C:\zd\azure-p
                 owershell\src\ResourceManager\Common\Commands.ResourceManager.Common\AzureRmCmdlet.cs:line 320
                    at Microsoft.Azure.Commands.Profile.GetAzureRMSubscriptionCommand.BeginProcessing() in C:\zd\azure-
                 powershell\src\ResourceManager\Profile\Commands.Profile\Subscription\GetAzureRMSubscription.cs:line 49
                    at System.Management.Automation.Cmdlet.DoBeginProcessing()
                    at System.Management.Automation.CommandProcessorBase.DoBegin()
Exception      : System.Management.Automation.PSInvalidOperationException
InvocationInfo : {Get-AzureRmSubscription}
Line           : Get-AzureRmSubscription
Position       : At line:1 char:1
                 + Get-AzureRmSubscription
                 + ~~~~~~~~~~~~~~~~~~~~~~~
HistoryId      : 5
```

<span data-ttu-id="ac972-114">Få information om alla fel som har inträffat i den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="ac972-114">Get details of all errors that have occurred in the current session.</span></span>

### <span data-ttu-id="ac972-115">Exempel 3: åtgärda ett specifikt fel</span><span class="sxs-lookup"><span data-stu-id="ac972-115">Example 3: Resolve a Specific Error</span></span>
```
PS C:\> Resolve-AzureRmError $Error[0]


   HistoryId: 8


RequestId      : b61309e8-09c9-4f0d-ba56-08a6b28c731d
Message        : Resource group 'contoso' could not be found.
ServerMessage  : ResourceGroupNotFound: Resource group 'contoso' could not be found.
                 (System.Collections.Generic.List`1[Microsoft.Rest.Azure.CloudError])
ServerResponse : {NotFound}
RequestMessage : {GET https://management.azure.com/subscriptions/00977cdb-163f-435f-9c32-39ec8ae61f4d/resourceGroups/co
                 ntoso/providers/Microsoft.Storage/storageAccounts/contoso?api-version=2016-12-01}
InvocationInfo : {Get-AzureRmStorageAccount}
Line           : Get-AzureRmStorageAccount -ResourceGroupName contoso -Name contoso
Position       : At line:1 char:1
                 + Get-AzureRmStorageAccount -ResourceGroupName contoso -Name contoso
                 + ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
StackTrace     :    at Microsoft.Azure.Management.Storage.StorageAccountsOperations.<GetPropertiesWithHttpMessagesAsync
                 >d__8.MoveNext()
                 --- End of stack trace from previous location where exception was thrown ---
                    at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
                    at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
                    at Microsoft.Azure.Management.Storage.StorageAccountsOperationsExtensions.<GetPropertiesAsync>d__7.
                 MoveNext()
                 --- End of stack trace from previous location where exception was thrown ---
                    at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
                    at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
                    at Microsoft.Azure.Management.Storage.StorageAccountsOperationsExtensions.GetProperties(IStorageAcc
                 ountsOperations operations, String resourceGroupName, String accountName)
                    at Microsoft.Azure.Commands.Management.Storage.GetAzureStorageAccountCommand.ExecuteCmdlet() in C:\
                 zd\azure-powershell\src\ResourceManager\Storage\Commands.Management.Storage\StorageAccount\GetAzureSto
                 rageAccount.cs:line 70
                    at Microsoft.WindowsAzure.Commands.Utilities.Common.AzurePSCmdlet.ProcessRecord() in
                 C:\zd\azure-powershell\src\Common\Commands.Common\AzurePSCmdlet.cs:line 642
HistoryId      : 8
```

<span data-ttu-id="ac972-116">Få information om det angivna felet.</span><span class="sxs-lookup"><span data-stu-id="ac972-116">Get details of the specified error.</span></span>

## <span data-ttu-id="ac972-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ac972-117">PARAMETERS</span></span>

### <span data-ttu-id="ac972-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac972-118">-DefaultProfile</span></span>
<span data-ttu-id="ac972-119">Autentiseringsuppgifter, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ac972-119">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac972-120">-Fel</span><span class="sxs-lookup"><span data-stu-id="ac972-120">-Error</span></span>
<span data-ttu-id="ac972-121">En eller flera fel poster att lösa.</span><span class="sxs-lookup"><span data-stu-id="ac972-121">One or more error records to resolve.</span></span>  <span data-ttu-id="ac972-122">Om inga parametrar anges löses alla fel i sessionen.</span><span class="sxs-lookup"><span data-stu-id="ac972-122">If no parameters are specified, all errors in the session are resolved.</span></span>

```yaml
Type: ErrorRecord[]
Parameter Sets: AnyErrorParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac972-123">-Senaste</span><span class="sxs-lookup"><span data-stu-id="ac972-123">-Last</span></span>
<span data-ttu-id="ac972-124">Lös bara det senaste felet som inträffade i sessionen.</span><span class="sxs-lookup"><span data-stu-id="ac972-124">Resolve only the last error that occurred in the session.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LastErrorParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac972-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac972-125">CommonParameters</span></span>
<span data-ttu-id="ac972-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac972-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac972-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac972-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac972-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ac972-128">INPUTS</span></span>

### <span data-ttu-id="ac972-129">System. Management. Automation. ErrorRecord []</span><span class="sxs-lookup"><span data-stu-id="ac972-129">System.Management.Automation.ErrorRecord[]</span></span>

## <span data-ttu-id="ac972-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ac972-130">OUTPUTS</span></span>

### <span data-ttu-id="ac972-131">Microsoft. Azure. commands. Profile. errors. AzureErrorRecord</span><span class="sxs-lookup"><span data-stu-id="ac972-131">Microsoft.Azure.Commands.Profile.Errors.AzureErrorRecord</span></span>
<span data-ttu-id="ac972-132">Information om ett PowerShell-fel som inte inbegriper en excpetion.</span><span class="sxs-lookup"><span data-stu-id="ac972-132">Information about a powershell error that does not involve an excpetion.</span></span>

### <span data-ttu-id="ac972-133">Microsoft. Azure. commands. Profile. errors. AzureExceptionRecord</span><span class="sxs-lookup"><span data-stu-id="ac972-133">Microsoft.Azure.Commands.Profile.Errors.AzureExceptionRecord</span></span>
<span data-ttu-id="ac972-134">Information om ett fel som innehåller detaljerad information om det undantag som utlöste felet.</span><span class="sxs-lookup"><span data-stu-id="ac972-134">Information about an error including detailed information on the exception that raised the error.</span></span>

### <span data-ttu-id="ac972-135">Microsoft. Azure. commands. Profile. errors. AzureRestExceptionRecord</span><span class="sxs-lookup"><span data-stu-id="ac972-135">Microsoft.Azure.Commands.Profile.Errors.AzureRestExceptionRecord</span></span>
<span data-ttu-id="ac972-136">Information om fel i cleint/server kommunikation.</span><span class="sxs-lookup"><span data-stu-id="ac972-136">Information about errors in cleint/server communications.</span></span>  <span data-ttu-id="ac972-137">Detta innehåller ofta viktig information om felet från servern.</span><span class="sxs-lookup"><span data-stu-id="ac972-137">This will often contain important information about the error from the server.</span></span>

## <span data-ttu-id="ac972-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ac972-138">NOTES</span></span>

## <span data-ttu-id="ac972-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ac972-139">RELATED LINKS</span></span>

