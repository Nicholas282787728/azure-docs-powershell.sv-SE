---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6187F603-5298-4854-94F3-0C38FCF3125F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupjobdetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJobDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJobDetails.md
ms.openlocfilehash: 109a02ac04fe9926ef4510d295c978e01026ade2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586399"
---
# <span data-ttu-id="536d8-101">Get-AzureRmBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="536d8-101">Get-AzureRmBackupJobDetails</span></span>

## <span data-ttu-id="536d8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="536d8-102">SYNOPSIS</span></span>
<span data-ttu-id="536d8-103">Hämtar information om ett säkerhets kopierings jobb.</span><span class="sxs-lookup"><span data-stu-id="536d8-103">Gets the details of a Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="536d8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="536d8-104">SYNTAX</span></span>

### <span data-ttu-id="536d8-105">JobsFiltersSet (standard)</span><span class="sxs-lookup"><span data-stu-id="536d8-105">JobsFiltersSet (Default)</span></span>
```
Get-AzureRmBackupJobDetails -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="536d8-106">IdFiltersSet</span><span class="sxs-lookup"><span data-stu-id="536d8-106">IdFiltersSet</span></span>
```
Get-AzureRmBackupJobDetails -Vault <AzureRMBackupVault> -JobId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="536d8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="536d8-107">DESCRIPTION</span></span>
<span data-ttu-id="536d8-108">Cmdleten **Get-AzureRmBackupJobDetails** hämtar information om ett Azure Backup-jobb.</span><span class="sxs-lookup"><span data-stu-id="536d8-108">The **Get-AzureRmBackupJobDetails** cmdlet gets the details of an Azure Backup job.</span></span>
<span data-ttu-id="536d8-109">Du kan använda denna cmdlet för att samla in information om ett jobb som Miss lyckas.</span><span class="sxs-lookup"><span data-stu-id="536d8-109">You can use this cmdlet to gather information about a job that fails.</span></span>

## <span data-ttu-id="536d8-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="536d8-110">EXAMPLES</span></span>

### <span data-ttu-id="536d8-111">Exempel 1: Visa information om ett misslyckat jobb</span><span class="sxs-lookup"><span data-stu-id="536d8-111">Example 1: Display the details of a failed job</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03" 
PS C:\> $Jobs = Get-AzureRmBackupJob -Vault $Vault -Status Failed
PS C:\> $JobDetails = Get-AzureRmBackupJobDetails -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
ErrorCode ErrorMessage                            Recommendations
--------- ------------                            ---------------
   400001 Command execution failed.               {Another operation is currently in p...
```

<span data-ttu-id="536d8-112">Det första kommandot får valvet med namnet Vault03 med hjälp av cmdleten **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="536d8-112">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="536d8-113">Kommandot lagrar objektet i $Vault variabel.</span><span class="sxs-lookup"><span data-stu-id="536d8-113">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="536d8-114">Det andra kommandot hämtar misslyckade jobb från valvet i $Vault och lagrar dem sedan i $Jobs mat ris variabel.</span><span class="sxs-lookup"><span data-stu-id="536d8-114">The second command gets failed jobs from the vault in $Vault, and then stores them in the $Jobs array variable.</span></span>

<span data-ttu-id="536d8-115">Det tredje jobbet får information om det första jobbet i $Jobs variabel och lagrar sedan informationen i $JobDetails variabel.</span><span class="sxs-lookup"><span data-stu-id="536d8-115">The third job gets details for the first job in the $Jobs variable, and then stores those details in the $JobDetails variable.</span></span>

<span data-ttu-id="536d8-116">Det sista kommandot visar egenskapen **ErrorDetails** för $JobDetails med standardsyntaxen för dot.</span><span class="sxs-lookup"><span data-stu-id="536d8-116">The final command displays the **ErrorDetails** property of $JobDetails by using standard dot syntax.</span></span>

### <span data-ttu-id="536d8-117">Exempel 2: Visa den rekommenderade åtgärden för ett misslyckat jobb</span><span class="sxs-lookup"><span data-stu-id="536d8-117">Example 2: Display the recommended action for a failed job</span></span>
```
PS C:\>$JobDetails.ErrorDetails.Recommendations
Another operation is currently in progress on this item. Please wait until the previous operation is completed, and then retry.
```

<span data-ttu-id="536d8-118">Det här kommandot visar den rekommenderade åtgärden från den $JobDetails variabel som skapades i det första exemplet.</span><span class="sxs-lookup"><span data-stu-id="536d8-118">This command displays the recommended action from the $JobDetails variable that was created in the first example.</span></span>

## <span data-ttu-id="536d8-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="536d8-119">PARAMETERS</span></span>

### <span data-ttu-id="536d8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="536d8-120">-DefaultProfile</span></span>
<span data-ttu-id="536d8-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="536d8-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="536d8-122">-Jobb</span><span class="sxs-lookup"><span data-stu-id="536d8-122">-Job</span></span>
<span data-ttu-id="536d8-123">Anger ett jobb som denna cmdlet får information om.</span><span class="sxs-lookup"><span data-stu-id="536d8-123">Specifies a job for which this cmdlet gets details.</span></span>
<span data-ttu-id="536d8-124">Använd Get-AzureRmBackupJob cmdlet för att få ett **AzureRmBackupJob** -objekt.</span><span class="sxs-lookup"><span data-stu-id="536d8-124">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: AzureRMBackupJob
Parameter Sets: JobsFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="536d8-125">-JobId</span><span class="sxs-lookup"><span data-stu-id="536d8-125">-JobId</span></span>
<span data-ttu-id="536d8-126">Anger ID för ett jobb som denna cmdlet hämtar information om.</span><span class="sxs-lookup"><span data-stu-id="536d8-126">Specifies the ID of a job for which this cmdlet gets details.</span></span>
<span data-ttu-id="536d8-127">ID är **InstanceID** -egenskapen för ett **AzureRmBackupJob** -objekt.</span><span class="sxs-lookup"><span data-stu-id="536d8-127">The ID is the **InstanceId** property of an **AzureRmBackupJob** object.</span></span>
<span data-ttu-id="536d8-128">För att få ett **AzureRmBackupJob** -objekt, Använd Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="536d8-128">To obtain an **AzureRmBackupJob** object, use Get-AzureRmBackupJob.</span></span>

```yaml
Type: String
Parameter Sets: IdFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="536d8-129">-Valv</span><span class="sxs-lookup"><span data-stu-id="536d8-129">-Vault</span></span>
<span data-ttu-id="536d8-130">Anger det säkerhets kopierings valv som denna cmdlet hämtar jobb uppgifter för.</span><span class="sxs-lookup"><span data-stu-id="536d8-130">Specifies the Backup vault for which this cmdlet gets job details.</span></span>
<span data-ttu-id="536d8-131">Använd Get-AzureRmBackupVault cmdlet för att få ett **AzureRmBackupVault** -objekt.</span><span class="sxs-lookup"><span data-stu-id="536d8-131">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: AzureRMBackupVault
Parameter Sets: IdFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="536d8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="536d8-132">CommonParameters</span></span>
<span data-ttu-id="536d8-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="536d8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="536d8-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="536d8-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="536d8-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="536d8-135">INPUTS</span></span>

### <span data-ttu-id="536d8-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="536d8-136">None</span></span>

## <span data-ttu-id="536d8-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="536d8-137">OUTPUTS</span></span>

### <span data-ttu-id="536d8-138">AzureRmBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="536d8-138">AzureRmBackupJobDetails</span></span>

## <span data-ttu-id="536d8-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="536d8-139">NOTES</span></span>
* <span data-ttu-id="536d8-140">Ingen</span><span class="sxs-lookup"><span data-stu-id="536d8-140">None</span></span>

## <span data-ttu-id="536d8-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="536d8-141">RELATED LINKS</span></span>

[<span data-ttu-id="536d8-142">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="536d8-142">Get-AzureRmBackupJob</span></span>](./Get-AzureRmBackupJob.md)

[<span data-ttu-id="536d8-143">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="536d8-143">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


