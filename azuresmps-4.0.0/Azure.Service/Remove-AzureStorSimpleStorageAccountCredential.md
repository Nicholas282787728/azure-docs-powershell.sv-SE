---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 1BD296FB-8BFC-473F-951D-D2BF265E50AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 048be9276957ee865aa3204392b1dd847b0d6acf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099679"
---
# <span data-ttu-id="6026d-101">Remove-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="6026d-101">Remove-AzureStorSimpleStorageAccountCredential</span></span>

## <span data-ttu-id="6026d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6026d-102">SYNOPSIS</span></span>
<span data-ttu-id="6026d-103">Tar bort en referens till ett befintligt lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="6026d-103">Deletes an existing storage account credential.</span></span>

## <span data-ttu-id="6026d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6026d-104">SYNTAX</span></span>

### <span data-ttu-id="6026d-105">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="6026d-105">IdentifyByName</span></span>
```
Remove-AzureStorSimpleStorageAccountCredential -StorageAccountName <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="6026d-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="6026d-106">IdentifyByObject</span></span>
```
Remove-AzureStorSimpleStorageAccountCredential -SAC <StorageAccountCredentialResponse> [-WaitForComplete]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6026d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6026d-107">DESCRIPTION</span></span>
<span data-ttu-id="6026d-108">Cmdleten **Remove-AzureStorSimpleStorageAccountCredential** tar bort en befintlig autentiseringsuppgift för lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="6026d-108">The **Remove-AzureStorSimpleStorageAccountCredential** cmdlet deletes an existing storage account credential.</span></span>
<span data-ttu-id="6026d-109">Ange ett konto med namn eller Använd cmdleten **Get-AzureStorSimpleStorageAccountCredential** för att hämta ett **StorageAccountCredential** -objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="6026d-109">Specify an account by name or use the **Get-AzureStorSimpleStorageAccountCredential** cmdlet to obtain a **StorageAccountCredential** object to delete.</span></span>

## <span data-ttu-id="6026d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6026d-110">EXAMPLES</span></span>

### <span data-ttu-id="6026d-111">Exempel 1: ta bort en autentiseringsuppgift för lagrings konto</span><span class="sxs-lookup"><span data-stu-id="6026d-111">Example 1: Remove a storage account credential</span></span>
```
PS C:\>Remove-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoStorage07" -Force
VERBOSE: ClientRequestId: 8e10d56b-ddb1-459b-b26e-a185f5a303de_PS
VERBOSE: About to create a job to remove your Storage Access Credential! 
VERBOSE: ClientRequestId: 55cb6296-0156-4266-8591-d9e9bf8cc584_PS
982f4b19-ccb0-4ad3-9b02-f8ad25bf2e72
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
982f4b19-ccb0-4ad3-9b02-f8ad25bf2e72 for tracking the task's status
```

<span data-ttu-id="6026d-112">Det här kommandot tar bort autentiseringsuppgifterna för lagrings kontot som heter ContosoStorage07.</span><span class="sxs-lookup"><span data-stu-id="6026d-112">This command removes the account credential for the storage account named ContosoStorage07.</span></span>
<span data-ttu-id="6026d-113">Det här kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="6026d-113">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="6026d-114">Cmdleten tar bort autentiseringsuppgiften utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="6026d-114">The cmdlet removes the credential without prompting your for confirmation.</span></span>

### <span data-ttu-id="6026d-115">Exempel 2: ta bort ett lagrings konto med hjälp av pipeline-operatorn</span><span class="sxs-lookup"><span data-stu-id="6026d-115">Example 2: Remove a storage account credential by using the pipeline operator</span></span>
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoStorage07" | Remove-AzureStorSimpleStorageAccountCredential -Force -WaitForComplete
VERBOSE: ClientRequestId: f1b46216-bf4c-4c19-8e92-1dfe3894e258_PS
VERBOSE: ClientRequestId: 0d946f8f-c771-4ade-8a83-7c08dad86c52_PS
VERBOSE: ClientRequestId: 2000bab6-8311-4192-ad12-c67e35fc2697_PS
VERBOSE: Storage Access Credential with name ContosoStorage07 found! 
VERBOSE: About to run a job to remove your Storage Access Credential! 
VERBOSE: ClientRequestId: b803b165-bef8-4a8f-9509-4b515ea8bdec_PS
VERBOSE: Your delete operation completed successfully!
```

<span data-ttu-id="6026d-116">Det här kommandot hämtar lagrings kontot med namnet ContosoStorage07 med hjälp av cmdleten **Get-AzureStorSimpleStorageAccountCredential** och skickar sedan objektet till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6026d-116">This command gets the storage account named ContosoStorage07 by using the **Get-AzureStorSimpleStorageAccountCredential** cmdlet, and then passes that object to the current cmdlet.</span></span>
<span data-ttu-id="6026d-117">Den aktuella cmdleten tar bort autentiseringsuppgiften för det lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="6026d-117">The current cmdlet removes the credential for that storage account.</span></span>
<span data-ttu-id="6026d-118">Det här kommandot anger parametern *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="6026d-118">This command specifies the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="6026d-119">Cmdleten återgår inte till konsolen förrän den slutförts.</span><span class="sxs-lookup"><span data-stu-id="6026d-119">The cmdlet does not return control to the console until it completes the remove operation.</span></span>

## <span data-ttu-id="6026d-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6026d-120">PARAMETERS</span></span>

### <span data-ttu-id="6026d-121">-Force</span><span class="sxs-lookup"><span data-stu-id="6026d-121">-Force</span></span>
<span data-ttu-id="6026d-122">Anger att du inte behöver bekräfta med den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6026d-122">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6026d-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="6026d-123">-Profile</span></span>
<span data-ttu-id="6026d-124">Anger en Azure-profil.</span><span class="sxs-lookup"><span data-stu-id="6026d-124">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6026d-125">-SAC</span><span class="sxs-lookup"><span data-stu-id="6026d-125">-SAC</span></span>
<span data-ttu-id="6026d-126">Anger autentiseringsuppgifter som ett **StorageAccountCredential** -objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="6026d-126">Specifies credential, as a **StorageAccountCredential** object, to remove.</span></span>
<span data-ttu-id="6026d-127">Om du vill hämta ett **StorageAccountCredential** -objekt använder du cmdleten **Get-AzureStorSimpleStorageAccountCredential** .</span><span class="sxs-lookup"><span data-stu-id="6026d-127">To obtain a **StorageAccountCredential** object, use the **Get-AzureStorSimpleStorageAccountCredential** cmdlet.</span></span>

```yaml
Type: StorageAccountCredentialResponse
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6026d-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6026d-128">-StorageAccountName</span></span>
<span data-ttu-id="6026d-129">Anger namnet på det lagrings konto som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="6026d-129">Specifies the name of the storage account credential to delete.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6026d-130">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="6026d-130">-WaitForComplete</span></span>
<span data-ttu-id="6026d-131">Anger att denna cmdlet väntar på att åtgärden ska slutföras innan den återfår kontroll till Windows PowerShell-konsolen.</span><span class="sxs-lookup"><span data-stu-id="6026d-131">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6026d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6026d-132">CommonParameters</span></span>
<span data-ttu-id="6026d-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6026d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6026d-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6026d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6026d-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6026d-135">INPUTS</span></span>

### <span data-ttu-id="6026d-136">StorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="6026d-136">StorageAccountCredential</span></span>
<span data-ttu-id="6026d-137">Denna cmdlet accepterar ett **StorageAccountCredential** -objekt med pipelinen.</span><span class="sxs-lookup"><span data-stu-id="6026d-137">This cmdlet accepts a **StorageAccountCredential** object by using the pipeline.</span></span>

## <span data-ttu-id="6026d-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6026d-138">OUTPUTS</span></span>

### <span data-ttu-id="6026d-139">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="6026d-139">TaskStatusInfo</span></span>
<span data-ttu-id="6026d-140">Denna cmdlet returnerar ett **TaskStatusInfo** -objekt om du anger parametern *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="6026d-140">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="6026d-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6026d-141">NOTES</span></span>

## <span data-ttu-id="6026d-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6026d-142">RELATED LINKS</span></span>

[<span data-ttu-id="6026d-143">Get-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="6026d-143">Get-AzureStorSimpleStorageAccountCredential</span></span>](./Get-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="6026d-144">New-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="6026d-144">New-AzureStorSimpleStorageAccountCredential</span></span>](./New-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="6026d-145">Set-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="6026d-145">Set-AzureStorSimpleStorageAccountCredential</span></span>](./Set-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="6026d-146">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="6026d-146">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


