---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7247CF85-78B0-4837-9162-F66077668A74
online version: ''
schema: 2.0.0
ms.openlocfilehash: d77dd294f386232f7db358696608aa47adceb1d2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099132"
---
# <span data-ttu-id="edba9-101">New-AzureSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="edba9-101">New-AzureSchedulerStorageQueueJob</span></span>

## <span data-ttu-id="edba9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="edba9-102">SYNOPSIS</span></span>
<span data-ttu-id="edba9-103">Skapar ett jobb i schemaläggare som har en lagrings åtgärd.</span><span class="sxs-lookup"><span data-stu-id="edba9-103">Creates a scheduler job that has a Storage action.</span></span>

## <span data-ttu-id="edba9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="edba9-104">SYNTAX</span></span>

### <span data-ttu-id="edba9-105">Kunna</span><span class="sxs-lookup"><span data-stu-id="edba9-105">Required</span></span>
```
New-AzureSchedulerStorageQueueJob -Location <String> -JobCollectionName <String> -JobName <String>
 -StorageQueueAccount <String> -StorageQueueName <String> -SASToken <String> [-StorageQueueMessage <String>]
 [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>] [-EndTime <DateTime>]
 [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionMethod <String>] [-ErrorActionURI <Uri>]
 [-ErrorActionRequestBody <String>] [-ErrorActionHeaders <Hashtable>] [-ErrorActionStorageAccount <String>]
 [-ErrorActionStorageQueue <String>] [-ErrorActionSASToken <String>] [-ErrorActionQueueMessageBody <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="edba9-106">Kommer</span><span class="sxs-lookup"><span data-stu-id="edba9-106">Recurring</span></span>
```
New-AzureSchedulerStorageQueueJob [-StorageQueueMessage <String>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionHeaders <Hashtable>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="edba9-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="edba9-107">DESCRIPTION</span></span>
<span data-ttu-id="edba9-108">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="edba9-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="edba9-109">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="edba9-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="edba9-110">Cmdleten **New-AzureSchedulerStorageQueueJob** skapar ett jobb i Schemaläggaren som har en Azure Storage-åtgärd.</span><span class="sxs-lookup"><span data-stu-id="edba9-110">The **New-AzureSchedulerStorageQueueJob** cmdlet creates a scheduler job that has an Azure Storage action.</span></span>

## <span data-ttu-id="edba9-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="edba9-111">EXAMPLES</span></span>

### <span data-ttu-id="edba9-112">Exempel 1: skapa ett lagrings jobb som körs en gång</span><span class="sxs-lookup"><span data-stu-id="edba9-112">Example 1: Create a Storage job that runs once</span></span>
```
PS C:\> New-AzureSchedulerStorageQueueJob -JobCollectionName "JobCollection01" -JobName "Job01" -Location "North Central US" -StorageQueueAccount "ContosoStorageAccount" -StorageQueueName "ContosoStorageQueue" -SASToken "?sv=2012-02-12&si=samplePolicy%2F30%2F2014%206%3A37%3A36%20PM&sig=vLQEbSfZbTFh7q3YrzlxBeL%2BjiYKp0gE6lMJ0a5Nb4M%3D"
```

<span data-ttu-id="edba9-113">Det här kommandot skapar ett lagrings jobb för schemaläggare som en del av samlingen med namnet JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="edba9-113">This command creates a scheduler Storage job as part of the collection named JobCollection01.</span></span>
<span data-ttu-id="edba9-114">Kommandot anger lagrings konto, könamn och SAS-token.</span><span class="sxs-lookup"><span data-stu-id="edba9-114">The command specifies the Storage account, queue name, and SAS token.</span></span>
<span data-ttu-id="edba9-115">Jobbet körs en gång omedelbart.</span><span class="sxs-lookup"><span data-stu-id="edba9-115">The job runs once, immediately.</span></span>

### <span data-ttu-id="edba9-116">Exempel 2: skapa ett lagrings jobb som kör ett angivet antal gånger</span><span class="sxs-lookup"><span data-stu-id="edba9-116">Example 2: Create a Storage job that runs a specified number of times</span></span>
```
PS C:\> New-AzureSchedulerStorageQueueJob -JobCollectionName "JobCollection01" -JobName "Job12" -Location "North Central US"-StorageQueueAccount "ContosoStorageAccount" -StorageQueueName "ContosoStorageQueue" -SASToken "?sv=2012-02-12&si=samplePolicy%2F30%2F2014%206%3A37%3A36%20PM&sig=vLQEbSfZbTFh7q3YrzlxBeL%2BjiYKp0gE6lMJ0a5Nb4M%3D" -ExecutionCount 20 -Frequency "Hour" -Interval 2
```

<span data-ttu-id="edba9-117">Det här kommandot skapar ett lagrings jobb för schemaläggare som en del av samlingen med namnet JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="edba9-117">This command creates a scheduler Storage job as part of the collection named JobCollection01.</span></span>
<span data-ttu-id="edba9-118">Kommandot anger lagrings konto, könamn och SAS-token.</span><span class="sxs-lookup"><span data-stu-id="edba9-118">The command specifies the Storage account, queue name, and SAS token.</span></span>
<span data-ttu-id="edba9-119">Jobbet körs 20 gånger totalt, två gånger per timme.</span><span class="sxs-lookup"><span data-stu-id="edba9-119">The job runs 20 times in total, twice every hour.</span></span>

## <span data-ttu-id="edba9-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="edba9-120">PARAMETERS</span></span>

### <span data-ttu-id="edba9-121">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="edba9-121">-EndTime</span></span>
<span data-ttu-id="edba9-122">Anger ett klock slag, som ett **datetime** -objekt, för Schemaläggaren att sluta initiera jobbet.</span><span class="sxs-lookup"><span data-stu-id="edba9-122">Specifies a time, as a **DateTime** object, for the scheduler to stop initiating the job.</span></span>
<span data-ttu-id="edba9-123">Använd cmdleten **Get-date** för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="edba9-123">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="edba9-124">Om du vill ha mer information skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="edba9-124">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="edba9-125">-ErrorActionHeaders</span><span class="sxs-lookup"><span data-stu-id="edba9-125">-ErrorActionHeaders</span></span>
<span data-ttu-id="edba9-126">Anger rubriker som en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="edba9-126">Specifies headers as a hash table.</span></span>

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

### <span data-ttu-id="edba9-127">-ErrorActionMethod</span><span class="sxs-lookup"><span data-stu-id="edba9-127">-ErrorActionMethod</span></span>
<span data-ttu-id="edba9-128">Anger metod för HTTP-och HTTPS-åtgärds typer.</span><span class="sxs-lookup"><span data-stu-id="edba9-128">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="edba9-129">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="edba9-129">Valid values are:</span></span> 

- <span data-ttu-id="edba9-130">LÄRA</span><span class="sxs-lookup"><span data-stu-id="edba9-130">GET</span></span>
- <span data-ttu-id="edba9-131">ÖRSEL</span><span class="sxs-lookup"><span data-stu-id="edba9-131">PUT</span></span>
- <span data-ttu-id="edba9-132">TEST</span><span class="sxs-lookup"><span data-stu-id="edba9-132">POST</span></span>
- <span data-ttu-id="edba9-133">HUVUDEN</span><span class="sxs-lookup"><span data-stu-id="edba9-133">HEAD</span></span>
- <span data-ttu-id="edba9-134">TA bort</span><span class="sxs-lookup"><span data-stu-id="edba9-134">DELETE</span></span>

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

### <span data-ttu-id="edba9-135">-ErrorActionQueueMessageBody</span><span class="sxs-lookup"><span data-stu-id="edba9-135">-ErrorActionQueueMessageBody</span></span>
<span data-ttu-id="edba9-136">Anger bröd texten för lagrings jobb åtgärder.</span><span class="sxs-lookup"><span data-stu-id="edba9-136">Specifies the body for Storage job actions.</span></span>

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

### <span data-ttu-id="edba9-137">-ErrorActionRequestBody</span><span class="sxs-lookup"><span data-stu-id="edba9-137">-ErrorActionRequestBody</span></span>
<span data-ttu-id="edba9-138">Anger brödtext för att placera och BOKFÖRA jobb åtgärder.</span><span class="sxs-lookup"><span data-stu-id="edba9-138">Specifies the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="edba9-139">-ErrorActionSASToken</span><span class="sxs-lookup"><span data-stu-id="edba9-139">-ErrorActionSASToken</span></span>
<span data-ttu-id="edba9-140">Anger den delade Access-signaturen (SAS) för lagrings kön.</span><span class="sxs-lookup"><span data-stu-id="edba9-140">Specifies the Shared Access Signature (SAS) token for the Storage queue.</span></span>

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

### <span data-ttu-id="edba9-141">-ErrorActionStorageAccount</span><span class="sxs-lookup"><span data-stu-id="edba9-141">-ErrorActionStorageAccount</span></span>
<span data-ttu-id="edba9-142">Anger namnet på lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="edba9-142">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="edba9-143">-ErrorActionStorageQueue</span><span class="sxs-lookup"><span data-stu-id="edba9-143">-ErrorActionStorageQueue</span></span>
<span data-ttu-id="edba9-144">Anger namnet på lagrings kön.</span><span class="sxs-lookup"><span data-stu-id="edba9-144">Specifies the name of the Storage queue.</span></span>

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

### <span data-ttu-id="edba9-145">-ErrorActionURI</span><span class="sxs-lookup"><span data-stu-id="edba9-145">-ErrorActionURI</span></span>
<span data-ttu-id="edba9-146">Anger URI för fel åtgärds åtgärden.</span><span class="sxs-lookup"><span data-stu-id="edba9-146">Specifies the URI for the error job action.</span></span>

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

### <span data-ttu-id="edba9-147">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="edba9-147">-ExecutionCount</span></span>
<span data-ttu-id="edba9-148">Anger antalet förekomster av ett jobb som körs.</span><span class="sxs-lookup"><span data-stu-id="edba9-148">Specifies the number occurrences of a job that run.</span></span>
<span data-ttu-id="edba9-149">Vanligt vis returnerar ett jobb oändligt.</span><span class="sxs-lookup"><span data-stu-id="edba9-149">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="edba9-150">-Frekvens</span><span class="sxs-lookup"><span data-stu-id="edba9-150">-Frequency</span></span>
<span data-ttu-id="edba9-151">Anger den maximala frekvensen för det här Schemaläggaren-jobbet.</span><span class="sxs-lookup"><span data-stu-id="edba9-151">Specifies the maximum frequency for this scheduler job.</span></span>

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

### <span data-ttu-id="edba9-152">-Intervall</span><span class="sxs-lookup"><span data-stu-id="edba9-152">-Interval</span></span>
<span data-ttu-id="edba9-153">Anger upprepnings intervallet för frekvensen som anges med hjälp av parametern *frekvens* .</span><span class="sxs-lookup"><span data-stu-id="edba9-153">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

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

### <span data-ttu-id="edba9-154">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="edba9-154">-JobCollectionName</span></span>
<span data-ttu-id="edba9-155">Anger namnet på den samling som ska innehålla jobbet schemaläggare.</span><span class="sxs-lookup"><span data-stu-id="edba9-155">Specifies the name of the collection to contain the scheduler job.</span></span>

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

### <span data-ttu-id="edba9-156">-JobName</span><span class="sxs-lookup"><span data-stu-id="edba9-156">-JobName</span></span>
<span data-ttu-id="edba9-157">Anger namnet på jobbet i Schemaläggaren.</span><span class="sxs-lookup"><span data-stu-id="edba9-157">Specifies the name for the scheduler job.</span></span>

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

### <span data-ttu-id="edba9-158">-JobState</span><span class="sxs-lookup"><span data-stu-id="edba9-158">-JobState</span></span>
<span data-ttu-id="edba9-159">Anger tillstånd för jobb i schemaläggare.</span><span class="sxs-lookup"><span data-stu-id="edba9-159">Specifies the state for the scheduler job.</span></span>

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

### <span data-ttu-id="edba9-160">-Plats</span><span class="sxs-lookup"><span data-stu-id="edba9-160">-Location</span></span>
<span data-ttu-id="edba9-161">Anger namnet på platsen där moln tjänsten är värd.</span><span class="sxs-lookup"><span data-stu-id="edba9-161">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="edba9-162">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="edba9-162">Valid values are:</span></span> 

- <span data-ttu-id="edba9-163">Världen över</span><span class="sxs-lookup"><span data-stu-id="edba9-163">Anywhere Asia</span></span>
- <span data-ttu-id="edba9-164">Överallt i Europa</span><span class="sxs-lookup"><span data-stu-id="edba9-164">Anywhere Europe</span></span>
- <span data-ttu-id="edba9-165">Var du än är</span><span class="sxs-lookup"><span data-stu-id="edba9-165">Anywhere US</span></span>
- <span data-ttu-id="edba9-166">Östasien</span><span class="sxs-lookup"><span data-stu-id="edba9-166">East Asia</span></span>
- <span data-ttu-id="edba9-167">Östra USA</span><span class="sxs-lookup"><span data-stu-id="edba9-167">East US</span></span>
- <span data-ttu-id="edba9-168">Norra Central USA</span><span class="sxs-lookup"><span data-stu-id="edba9-168">North Central US</span></span>
- <span data-ttu-id="edba9-169">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="edba9-169">North Europe</span></span>
- <span data-ttu-id="edba9-170">Södra centrala USA</span><span class="sxs-lookup"><span data-stu-id="edba9-170">South Central US</span></span>
- <span data-ttu-id="edba9-171">Sydostasien</span><span class="sxs-lookup"><span data-stu-id="edba9-171">Southeast Asia</span></span>
- <span data-ttu-id="edba9-172">Västeuropa</span><span class="sxs-lookup"><span data-stu-id="edba9-172">West Europe</span></span>
- <span data-ttu-id="edba9-173">Västra USA</span><span class="sxs-lookup"><span data-stu-id="edba9-173">West US</span></span>

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

### <span data-ttu-id="edba9-174">-Profil</span><span class="sxs-lookup"><span data-stu-id="edba9-174">-Profile</span></span>
<span data-ttu-id="edba9-175">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="edba9-175">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="edba9-176">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="edba9-176">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="edba9-177">-SASToken</span><span class="sxs-lookup"><span data-stu-id="edba9-177">-SASToken</span></span>
<span data-ttu-id="edba9-178">Anger SAS-token för lagrings kön.</span><span class="sxs-lookup"><span data-stu-id="edba9-178">Specifies the SAS token for the Storage queue.</span></span>

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

### <span data-ttu-id="edba9-179">-StartTime</span><span class="sxs-lookup"><span data-stu-id="edba9-179">-StartTime</span></span>
<span data-ttu-id="edba9-180">Anger ett klock slag, som ett **datetime** -objekt, för jobbet som ska starta.</span><span class="sxs-lookup"><span data-stu-id="edba9-180">Specifies a time, as a **DateTime** object, for the job to start.</span></span>

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

### <span data-ttu-id="edba9-181">-StorageQueueAccount</span><span class="sxs-lookup"><span data-stu-id="edba9-181">-StorageQueueAccount</span></span>
<span data-ttu-id="edba9-182">Anger namnet på lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="edba9-182">Specifies the Storage account name.</span></span>

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

### <span data-ttu-id="edba9-183">-StorageQueueMessage</span><span class="sxs-lookup"><span data-stu-id="edba9-183">-StorageQueueMessage</span></span>
<span data-ttu-id="edba9-184">Anger Kömeddelanden för lagrings jobb.</span><span class="sxs-lookup"><span data-stu-id="edba9-184">Specifies the queue message for Storage job.</span></span>

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

### <span data-ttu-id="edba9-185">-StorageQueueName</span><span class="sxs-lookup"><span data-stu-id="edba9-185">-StorageQueueName</span></span>
<span data-ttu-id="edba9-186">Anger namnet på lagrings kön.</span><span class="sxs-lookup"><span data-stu-id="edba9-186">Specifies the name of the Storage queue.</span></span>

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

### <span data-ttu-id="edba9-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edba9-187">CommonParameters</span></span>
<span data-ttu-id="edba9-188">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edba9-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edba9-189">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edba9-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edba9-190">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="edba9-190">INPUTS</span></span>

## <span data-ttu-id="edba9-191">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="edba9-191">OUTPUTS</span></span>

## <span data-ttu-id="edba9-192">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="edba9-192">NOTES</span></span>

## <span data-ttu-id="edba9-193">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="edba9-193">RELATED LINKS</span></span>

[<span data-ttu-id="edba9-194">Set-AzureSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="edba9-194">Set-AzureSchedulerStorageQueueJob</span></span>](./Set-AzureSchedulerStorageQueueJob.md)


