---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8D53014E-B32D-4A37-8C49-E7BA6217A228
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7b4f8fb409d0bde379c3d4b57cf5f19a73fbd4e3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099280"
---
# <span data-ttu-id="3d638-101">Set-AzureSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="3d638-101">Set-AzureSchedulerStorageQueueJob</span></span>

## <span data-ttu-id="3d638-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3d638-102">SYNOPSIS</span></span>
<span data-ttu-id="3d638-103">Uppdaterar ett jobb i Schemaläggaren som har en lagrings åtgärd.</span><span class="sxs-lookup"><span data-stu-id="3d638-103">Updates a scheduler job that has a storage action.</span></span>

## <span data-ttu-id="3d638-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3d638-104">SYNTAX</span></span>

### <span data-ttu-id="3d638-105">Kunna</span><span class="sxs-lookup"><span data-stu-id="3d638-105">Required</span></span>
```
Set-AzureSchedulerStorageQueueJob -Location <String> -JobCollectionName <String> -JobName <String>
 [-StorageQueueAccount <String>] [-StorageQueueName <String>] [-SASToken <String>]
 [-StorageQueueMessage <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionMethod <String>]
 [-ErrorActionURI <Uri>] [-ErrorActionRequestBody <String>] [-ErrorActionHeaders <Hashtable>]
 [-ErrorActionStorageAccount <String>] [-ErrorActionStorageQueue <String>] [-ErrorActionSASToken <String>]
 [-ErrorActionQueueMessageBody <String>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3d638-106">Kommer</span><span class="sxs-lookup"><span data-stu-id="3d638-106">Recurring</span></span>
```
Set-AzureSchedulerStorageQueueJob [-Interval <Int32>] [-Frequency <String>] [-EndTime <DateTime>]
 [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionHeaders <Hashtable>] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3d638-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3d638-107">DESCRIPTION</span></span>
<span data-ttu-id="3d638-108">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="3d638-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="3d638-109">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="3d638-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="3d638-110">Cmdleten **set-AzureSchedulerStorageQueueJob** uppdaterar ett jobb i Schemaläggaren som har en Azure Storage-åtgärd.</span><span class="sxs-lookup"><span data-stu-id="3d638-110">The **Set-AzureSchedulerStorageQueueJob** cmdlet updates a scheduler job that has an Azure Storage action.</span></span>

## <span data-ttu-id="3d638-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3d638-111">EXAMPLES</span></span>

### <span data-ttu-id="3d638-112">Exempel 1: uppdatera ett meddelande i kö</span><span class="sxs-lookup"><span data-stu-id="3d638-112">Example 1: Update a Storage queue message</span></span>
```
PS C:\> Set-AzureSchedulerStorageQueueJob -Location "North Central US" -JobCollectionName "JobCollection01 -JobName "Job12" -StorageQueueMessage "Updated message"
```

<span data-ttu-id="3d638-113">Det här kommandot uppdaterar Kömeddelanden för lagrings jobbet med namnet Job12.</span><span class="sxs-lookup"><span data-stu-id="3d638-113">This command updates the queue message for the Storage job named Job12.</span></span>
<span data-ttu-id="3d638-114">Kommandot anger jobbnamn och plats.</span><span class="sxs-lookup"><span data-stu-id="3d638-114">The command specifies the job collection name and the location.</span></span>

### <span data-ttu-id="3d638-115">Exempel 2: aktivera ett utskrifts jobb</span><span class="sxs-lookup"><span data-stu-id="3d638-115">Example 2: Enable a Storage queue job</span></span>
```
PS C:\> Set-AzureSchedulerStorageQueueJob -Location "North Central US" -JobCollectionName "JobCollection02" -JobName "Job16" -JobState "Enabled"
```

<span data-ttu-id="3d638-116">Det här kommandot aktiverar jobbet med namnet Job16.</span><span class="sxs-lookup"><span data-stu-id="3d638-116">This command enables the job named Job16.</span></span>
<span data-ttu-id="3d638-117">Kommandot ändrar läget för jobbet till aktiverat genom att ange det värdet för parametern *JobState* .</span><span class="sxs-lookup"><span data-stu-id="3d638-117">The command changes the state of the job to Enabled by specifying that value for the *JobState* parameter.</span></span>

## <span data-ttu-id="3d638-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3d638-118">PARAMETERS</span></span>

### <span data-ttu-id="3d638-119">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="3d638-119">-EndTime</span></span>
<span data-ttu-id="3d638-120">Anger ett klock slag, som ett **datetime** -objekt, för Schemaläggaren att sluta initiera jobbet.</span><span class="sxs-lookup"><span data-stu-id="3d638-120">Specifies a time, as a **DateTime** object, for the scheduler to stop initiating the job.</span></span>
<span data-ttu-id="3d638-121">Använd cmdleten **Get-date** för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="3d638-121">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="3d638-122">Om du vill ha mer information skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="3d638-122">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d638-123">-ErrorActionHeaders</span><span class="sxs-lookup"><span data-stu-id="3d638-123">-ErrorActionHeaders</span></span>
<span data-ttu-id="3d638-124">Anger rubriker som en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="3d638-124">Specifies headers as a hash table.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d638-125">-ErrorActionMethod</span><span class="sxs-lookup"><span data-stu-id="3d638-125">-ErrorActionMethod</span></span>
<span data-ttu-id="3d638-126">Anger metod för HTTP-och HTTPS-åtgärds typer.</span><span class="sxs-lookup"><span data-stu-id="3d638-126">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="3d638-127">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="3d638-127">Valid values are:</span></span> 

- <span data-ttu-id="3d638-128">LÄRA</span><span class="sxs-lookup"><span data-stu-id="3d638-128">GET</span></span>
- <span data-ttu-id="3d638-129">ÖRSEL</span><span class="sxs-lookup"><span data-stu-id="3d638-129">PUT</span></span>
- <span data-ttu-id="3d638-130">TEST</span><span class="sxs-lookup"><span data-stu-id="3d638-130">POST</span></span>
- <span data-ttu-id="3d638-131">HUVUDEN</span><span class="sxs-lookup"><span data-stu-id="3d638-131">HEAD</span></span>
- <span data-ttu-id="3d638-132">TA bort</span><span class="sxs-lookup"><span data-stu-id="3d638-132">DELETE</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d638-133">-ErrorActionQueueMessageBody</span><span class="sxs-lookup"><span data-stu-id="3d638-133">-ErrorActionQueueMessageBody</span></span>
<span data-ttu-id="3d638-134">Anger bröd texten för lagrings jobb åtgärder.</span><span class="sxs-lookup"><span data-stu-id="3d638-134">Specifies the body for Storage job actions.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d638-135">-ErrorActionRequestBody</span><span class="sxs-lookup"><span data-stu-id="3d638-135">-ErrorActionRequestBody</span></span>
<span data-ttu-id="3d638-136">Anger brödtext för att placera och BOKFÖRA jobb åtgärder.</span><span class="sxs-lookup"><span data-stu-id="3d638-136">Specifies the body for PUT and POST job actions.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d638-137">-ErrorActionSASToken</span><span class="sxs-lookup"><span data-stu-id="3d638-137">-ErrorActionSASToken</span></span>
<span data-ttu-id="3d638-138">Anger den delade Access-signaturen (SAS) för lagrings kön.</span><span class="sxs-lookup"><span data-stu-id="3d638-138">Specifies the Shared Access Signature (SAS) token for the Storage queue.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d638-139">-ErrorActionStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3d638-139">-ErrorActionStorageAccount</span></span>
<span data-ttu-id="3d638-140">Anger namnet på lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="3d638-140">Specifies the name of the Storage account.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d638-141">-ErrorActionStorageQueue</span><span class="sxs-lookup"><span data-stu-id="3d638-141">-ErrorActionStorageQueue</span></span>
<span data-ttu-id="3d638-142">Anger namnet på lagrings kön.</span><span class="sxs-lookup"><span data-stu-id="3d638-142">Specifies the name of the Storage queue.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d638-143">-ErrorActionURI</span><span class="sxs-lookup"><span data-stu-id="3d638-143">-ErrorActionURI</span></span>
<span data-ttu-id="3d638-144">Anger URI för fel åtgärds åtgärden.</span><span class="sxs-lookup"><span data-stu-id="3d638-144">Specifies the URI for the error job action.</span></span>

```yaml
Type: Uri
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d638-145">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="3d638-145">-ExecutionCount</span></span>
<span data-ttu-id="3d638-146">Anger antalet förekomster av ett jobb som körs.</span><span class="sxs-lookup"><span data-stu-id="3d638-146">Specifies the number occurrences of a job that run.</span></span>
<span data-ttu-id="3d638-147">Vanligt vis returnerar ett jobb oändligt.</span><span class="sxs-lookup"><span data-stu-id="3d638-147">By default, a job recurs indefinitely.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d638-148">-Frekvens</span><span class="sxs-lookup"><span data-stu-id="3d638-148">-Frequency</span></span>
<span data-ttu-id="3d638-149">Anger den maximala frekvensen för det här Schemaläggaren-jobbet.</span><span class="sxs-lookup"><span data-stu-id="3d638-149">Specifies the maximum frequency for this scheduler job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d638-150">-Intervall</span><span class="sxs-lookup"><span data-stu-id="3d638-150">-Interval</span></span>
<span data-ttu-id="3d638-151">Anger upprepnings intervallet för frekvensen som anges med hjälp av parametern *frekvens* .</span><span class="sxs-lookup"><span data-stu-id="3d638-151">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d638-152">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="3d638-152">-JobCollectionName</span></span>
<span data-ttu-id="3d638-153">Anger namnet på den samling som ska innehålla jobbet schemaläggare.</span><span class="sxs-lookup"><span data-stu-id="3d638-153">Specifies the name of the collection to contain the scheduler job.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d638-154">-JobName</span><span class="sxs-lookup"><span data-stu-id="3d638-154">-JobName</span></span>
<span data-ttu-id="3d638-155">Anger namnet på det jobb i Schemaläggaren som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="3d638-155">Specifies the name of the scheduler job to update.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d638-156">-JobState</span><span class="sxs-lookup"><span data-stu-id="3d638-156">-JobState</span></span>
<span data-ttu-id="3d638-157">Anger tillstånd för jobb i schemaläggare.</span><span class="sxs-lookup"><span data-stu-id="3d638-157">Specifies the state for the scheduler job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d638-158">-Plats</span><span class="sxs-lookup"><span data-stu-id="3d638-158">-Location</span></span>
<span data-ttu-id="3d638-159">Anger namnet på platsen där moln tjänsten är värd.</span><span class="sxs-lookup"><span data-stu-id="3d638-159">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="3d638-160">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="3d638-160">Valid values are:</span></span> 

- <span data-ttu-id="3d638-161">Världen över</span><span class="sxs-lookup"><span data-stu-id="3d638-161">Anywhere Asia</span></span>
- <span data-ttu-id="3d638-162">Överallt i Europa</span><span class="sxs-lookup"><span data-stu-id="3d638-162">Anywhere Europe</span></span>
- <span data-ttu-id="3d638-163">Var du än är</span><span class="sxs-lookup"><span data-stu-id="3d638-163">Anywhere US</span></span>
- <span data-ttu-id="3d638-164">Östasien</span><span class="sxs-lookup"><span data-stu-id="3d638-164">East Asia</span></span>
- <span data-ttu-id="3d638-165">Östra USA</span><span class="sxs-lookup"><span data-stu-id="3d638-165">East US</span></span>
- <span data-ttu-id="3d638-166">Norra Central USA</span><span class="sxs-lookup"><span data-stu-id="3d638-166">North Central US</span></span>
- <span data-ttu-id="3d638-167">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="3d638-167">North Europe</span></span>
- <span data-ttu-id="3d638-168">Södra centrala USA</span><span class="sxs-lookup"><span data-stu-id="3d638-168">South Central US</span></span>
- <span data-ttu-id="3d638-169">Sydostasien</span><span class="sxs-lookup"><span data-stu-id="3d638-169">Southeast Asia</span></span>
- <span data-ttu-id="3d638-170">Västeuropa</span><span class="sxs-lookup"><span data-stu-id="3d638-170">West Europe</span></span>
- <span data-ttu-id="3d638-171">Västra USA</span><span class="sxs-lookup"><span data-stu-id="3d638-171">West US</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d638-172">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3d638-172">-PassThru</span></span>
<span data-ttu-id="3d638-173">Anger att den här cmdleten returnerar ett objekt som representerar det objekt som den körs på.</span><span class="sxs-lookup"><span data-stu-id="3d638-173">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="3d638-174">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="3d638-174">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3d638-175">-Profil</span><span class="sxs-lookup"><span data-stu-id="3d638-175">-Profile</span></span>
<span data-ttu-id="3d638-176">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="3d638-176">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3d638-177">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="3d638-177">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3d638-178">-SASToken</span><span class="sxs-lookup"><span data-stu-id="3d638-178">-SASToken</span></span>
<span data-ttu-id="3d638-179">Anger SAS-token för lagrings kön.</span><span class="sxs-lookup"><span data-stu-id="3d638-179">Specifies the SAS token for the Storage queue.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d638-180">-StartTime</span><span class="sxs-lookup"><span data-stu-id="3d638-180">-StartTime</span></span>
<span data-ttu-id="3d638-181">Anger ett klock slag, som ett **datetime** -objekt, för jobbet som ska starta.</span><span class="sxs-lookup"><span data-stu-id="3d638-181">Specifies a time, as a **DateTime** object, for the job to start.</span></span>

```yaml
Type: DateTime
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d638-182">-StorageQueueAccount</span><span class="sxs-lookup"><span data-stu-id="3d638-182">-StorageQueueAccount</span></span>
<span data-ttu-id="3d638-183">Anger namnet på lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="3d638-183">Specifies the Storage account name.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d638-184">-StorageQueueMessage</span><span class="sxs-lookup"><span data-stu-id="3d638-184">-StorageQueueMessage</span></span>
<span data-ttu-id="3d638-185">Anger köns meddelande för lagrings jobbet.</span><span class="sxs-lookup"><span data-stu-id="3d638-185">Specifies the queue message for the Storage job.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d638-186">-StorageQueueName</span><span class="sxs-lookup"><span data-stu-id="3d638-186">-StorageQueueName</span></span>
<span data-ttu-id="3d638-187">Anger namnet på lagrings kön.</span><span class="sxs-lookup"><span data-stu-id="3d638-187">Specifies the name of the Storage queue.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d638-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d638-188">CommonParameters</span></span>
<span data-ttu-id="3d638-189">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d638-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d638-190">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d638-190">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d638-191">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3d638-191">INPUTS</span></span>

## <span data-ttu-id="3d638-192">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3d638-192">OUTPUTS</span></span>

## <span data-ttu-id="3d638-193">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3d638-193">NOTES</span></span>

## <span data-ttu-id="3d638-194">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3d638-194">RELATED LINKS</span></span>

[<span data-ttu-id="3d638-195">New-AzureSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="3d638-195">New-AzureSchedulerStorageQueueJob</span></span>](./New-AzureSchedulerStorageQueueJob.md)


