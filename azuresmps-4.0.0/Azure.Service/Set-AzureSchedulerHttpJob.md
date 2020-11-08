---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: BBB1A0B7-2F5A-4799-8375-1D775C9D6E2F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 935d9ace51144cdd54cbcf3348ed9fc6b9b4ea02
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099029"
---
# <span data-ttu-id="64275-101">Set-AzureSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="64275-101">Set-AzureSchedulerHttpJob</span></span>

## <span data-ttu-id="64275-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="64275-102">SYNOPSIS</span></span>
<span data-ttu-id="64275-103">Uppdaterar ett jobb i schemaläggare som har en HTTP-åtgärd.</span><span class="sxs-lookup"><span data-stu-id="64275-103">Updates a scheduler job that has an HTTP action.</span></span>

## <span data-ttu-id="64275-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="64275-104">SYNTAX</span></span>

### <span data-ttu-id="64275-105">Kunna</span><span class="sxs-lookup"><span data-stu-id="64275-105">Required</span></span>
```
Set-AzureSchedulerHttpJob -Location <String> -JobCollectionName <String> -JobName <String> [-Method <String>]
 [-URI <Uri>] [-RequestBody <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-ExecutionCount <Int32>] [-EndTime <DateTime>] [-JobState <String>] [-Headers <Hashtable>]
 [-ErrorActionMethod <String>] [-ErrorActionURI <Uri>] [-ErrorActionRequestBody <String>]
 [-ErrorActionHeaders <Hashtable>] [-ErrorActionStorageAccount <String>] [-ErrorActionStorageQueue <String>]
 [-ErrorActionSASToken <String>] [-ErrorActionQueueMessageBody <String>] [-HttpAuthenticationType <String>]
 [-ClientCertificatePfx <Object>] [-ClientCertificatePassword <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="64275-106">PutPost</span><span class="sxs-lookup"><span data-stu-id="64275-106">PutPost</span></span>
```
Set-AzureSchedulerHttpJob [-RequestBody <String>] [-JobState <String>] [-Headers <Hashtable>]
 [-ErrorActionHeaders <Hashtable>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="64275-107">Kommer</span><span class="sxs-lookup"><span data-stu-id="64275-107">Recurring</span></span>
```
Set-AzureSchedulerHttpJob [-Interval <Int32>] [-Frequency <String>] [-ExecutionCount <Int32>]
 [-EndTime <DateTime>] [-JobState <String>] [-Headers <Hashtable>] [-ErrorActionHeaders <Hashtable>]
 [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="64275-108">Verifieringsmetoden</span><span class="sxs-lookup"><span data-stu-id="64275-108">Authentication</span></span>
```
Set-AzureSchedulerHttpJob [-JobState <String>] [-Headers <Hashtable>] [-ErrorActionHeaders <Hashtable>]
 -HttpAuthenticationType <String> [-ClientCertificatePfx <Object>] [-ClientCertificatePassword <String>]
 [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="64275-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="64275-109">DESCRIPTION</span></span>
<span data-ttu-id="64275-110">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="64275-110">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="64275-111">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="64275-111">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="64275-112">Cmdleten **set-AzureSchedulerHttpJob** uppdaterar ett jobb i schemaläggare som har en HTTP-åtgärd.</span><span class="sxs-lookup"><span data-stu-id="64275-112">The **Set-AzureSchedulerHttpJob** cmdlet updates a scheduler job that has an HTTP action.</span></span>

## <span data-ttu-id="64275-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="64275-113">EXAMPLES</span></span>

### <span data-ttu-id="64275-114">Exempel 1: ändra tillståndet för ett jobb till inaktiverat</span><span class="sxs-lookup"><span data-stu-id="64275-114">Example 1: Change the state of a job to Disabled</span></span>
```
PS C:\> Set-AzureSchedulerHttpJob -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job01" -JobState "Disabled"
```

<span data-ttu-id="64275-115">Det här kommandot ändrar status för jobbet som heter Job01 till disabled.</span><span class="sxs-lookup"><span data-stu-id="64275-115">This command changes the state of the job named Job01 to Disabled.</span></span>
<span data-ttu-id="64275-116">Jobbet ingår i jobb samlingen med namnet JobColleciton01 för den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="64275-116">That job is part of the job collection named JobColleciton01 for the specified location.</span></span>

### <span data-ttu-id="64275-117">Exempel 2: uppdatera URI för ett jobb</span><span class="sxs-lookup"><span data-stu-id="64275-117">Example 2: Update the URI of a job</span></span>
```
PS C:\> Set-AzureSchedulerHttpJob -Location "North Central US" -JobCollectionName "JobCollection02" -JobName "Job37" -URI http://www.contoso.com
```

<span data-ttu-id="64275-118">Det här kommandot uppdaterar URI för jobbet som heter Job01 http://www.contoso.com .</span><span class="sxs-lookup"><span data-stu-id="64275-118">This command updates the URI of the job named Job01 to be http://www.contoso.com.</span></span>

## <span data-ttu-id="64275-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="64275-119">PARAMETERS</span></span>

### <span data-ttu-id="64275-120">-ClientCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="64275-120">-ClientCertificatePassword</span></span>
```yaml
Type: String
Parameter Sets: Required, Authentication
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64275-121">-ClientCertificatePfx</span><span class="sxs-lookup"><span data-stu-id="64275-121">-ClientCertificatePfx</span></span>
```yaml
Type: Object
Parameter Sets: Required, Authentication
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64275-122">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="64275-122">-EndTime</span></span>
<span data-ttu-id="64275-123">Anger ett klock slag, som ett **datetime** -objekt, för Schemaläggaren att sluta initiera jobb.</span><span class="sxs-lookup"><span data-stu-id="64275-123">Specifies a time, as a **DateTime** object, for the scheduler to stop initiating jobs.</span></span>
<span data-ttu-id="64275-124">Använd cmdleten **Get-date** för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="64275-124">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="64275-125">Om du vill ha mer information skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="64275-125">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: Required, Recurring
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64275-126">-ErrorActionHeaders</span><span class="sxs-lookup"><span data-stu-id="64275-126">-ErrorActionHeaders</span></span>
<span data-ttu-id="64275-127">Anger rubriker som en hash-gruppnamn.</span><span class="sxs-lookup"><span data-stu-id="64275-127">Specifies headers as a hashtable.</span></span>

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

### <span data-ttu-id="64275-128">-ErrorActionMethod</span><span class="sxs-lookup"><span data-stu-id="64275-128">-ErrorActionMethod</span></span>
<span data-ttu-id="64275-129">Anger metod för HTTP-och HTTPS-åtgärds typer.</span><span class="sxs-lookup"><span data-stu-id="64275-129">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="64275-130">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="64275-130">Valid values are:</span></span> 

- <span data-ttu-id="64275-131">LÄRA</span><span class="sxs-lookup"><span data-stu-id="64275-131">GET</span></span>
- <span data-ttu-id="64275-132">ÖRSEL</span><span class="sxs-lookup"><span data-stu-id="64275-132">PUT</span></span>
- <span data-ttu-id="64275-133">TEST</span><span class="sxs-lookup"><span data-stu-id="64275-133">POST</span></span>
- <span data-ttu-id="64275-134">HUVUDEN</span><span class="sxs-lookup"><span data-stu-id="64275-134">HEAD</span></span>
- <span data-ttu-id="64275-135">TA bort</span><span class="sxs-lookup"><span data-stu-id="64275-135">DELETE</span></span>

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

### <span data-ttu-id="64275-136">-ErrorActionQueueMessageBody</span><span class="sxs-lookup"><span data-stu-id="64275-136">-ErrorActionQueueMessageBody</span></span>
<span data-ttu-id="64275-137">Anger bröd texten för lagrings jobb åtgärder.</span><span class="sxs-lookup"><span data-stu-id="64275-137">Specifies the body for storage job actions.</span></span>

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

### <span data-ttu-id="64275-138">-ErrorActionRequestBody</span><span class="sxs-lookup"><span data-stu-id="64275-138">-ErrorActionRequestBody</span></span>
<span data-ttu-id="64275-139">Anger brödtext för att placera och BOKFÖRA jobb åtgärder.</span><span class="sxs-lookup"><span data-stu-id="64275-139">Specifies the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="64275-140">-ErrorActionSASToken</span><span class="sxs-lookup"><span data-stu-id="64275-140">-ErrorActionSASToken</span></span>
<span data-ttu-id="64275-141">Anger den delade Access-signaturen (SAS) för lagrings kön.</span><span class="sxs-lookup"><span data-stu-id="64275-141">Specifies the Shared Access Signature (SAS) token for the storage queue.</span></span>

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

### <span data-ttu-id="64275-142">-ErrorActionStorageAccount</span><span class="sxs-lookup"><span data-stu-id="64275-142">-ErrorActionStorageAccount</span></span>
<span data-ttu-id="64275-143">Anger namnet på lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="64275-143">Specifies the name of the storage account.</span></span>

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

### <span data-ttu-id="64275-144">-ErrorActionStorageQueue</span><span class="sxs-lookup"><span data-stu-id="64275-144">-ErrorActionStorageQueue</span></span>
<span data-ttu-id="64275-145">Anger namnet på lagrings kön.</span><span class="sxs-lookup"><span data-stu-id="64275-145">Specifies the name of the storage queue.</span></span>

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

### <span data-ttu-id="64275-146">-ErrorActionURI</span><span class="sxs-lookup"><span data-stu-id="64275-146">-ErrorActionURI</span></span>
<span data-ttu-id="64275-147">Anger URI för fel åtgärds åtgärden.</span><span class="sxs-lookup"><span data-stu-id="64275-147">Specifies the URI for the error job action.</span></span>

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

### <span data-ttu-id="64275-148">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="64275-148">-ExecutionCount</span></span>
<span data-ttu-id="64275-149">Anger antalet förekomster av ett jobb som körs.</span><span class="sxs-lookup"><span data-stu-id="64275-149">Specifies the number occurrences of a job that run.</span></span>
<span data-ttu-id="64275-150">Vanligt vis returnerar ett jobb oändligt.</span><span class="sxs-lookup"><span data-stu-id="64275-150">By default, a job recurs indefinitely.</span></span>

```yaml
Type: Int32
Parameter Sets: Required, Recurring
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64275-151">-Frekvens</span><span class="sxs-lookup"><span data-stu-id="64275-151">-Frequency</span></span>
<span data-ttu-id="64275-152">Anger den maximala frekvensen för det här Schemaläggaren-jobbet.</span><span class="sxs-lookup"><span data-stu-id="64275-152">Specifies the maximum frequency for this scheduler job.</span></span>

```yaml
Type: String
Parameter Sets: Required, Recurring
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64275-153">-Rubriker</span><span class="sxs-lookup"><span data-stu-id="64275-153">-Headers</span></span>
<span data-ttu-id="64275-154">Anger huvudena som en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="64275-154">Specifies the headers as a hash table.</span></span>

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

### <span data-ttu-id="64275-155">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="64275-155">-HttpAuthenticationType</span></span>
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

```yaml
Type: String
Parameter Sets: Authentication
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64275-156">-Intervall</span><span class="sxs-lookup"><span data-stu-id="64275-156">-Interval</span></span>
<span data-ttu-id="64275-157">Anger upprepnings intervallet för frekvensen som anges med hjälp av parametern *frekvens* .</span><span class="sxs-lookup"><span data-stu-id="64275-157">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: Required, Recurring
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64275-158">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="64275-158">-JobCollectionName</span></span>
<span data-ttu-id="64275-159">Anger namnet på den mängd som innehåller Schemaläggaren-jobbet som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="64275-159">Specifies the name of the collection that contains the scheduler job to modify.</span></span>

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

### <span data-ttu-id="64275-160">-JobName</span><span class="sxs-lookup"><span data-stu-id="64275-160">-JobName</span></span>
<span data-ttu-id="64275-161">Anger namnet på det jobb som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="64275-161">Specifies the name of scheduler job to modify.</span></span>

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

### <span data-ttu-id="64275-162">-JobState</span><span class="sxs-lookup"><span data-stu-id="64275-162">-JobState</span></span>
<span data-ttu-id="64275-163">Anger tillstånd för jobb i schemaläggare.</span><span class="sxs-lookup"><span data-stu-id="64275-163">Specifies the state for the scheduler job.</span></span>

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

### <span data-ttu-id="64275-164">-Plats</span><span class="sxs-lookup"><span data-stu-id="64275-164">-Location</span></span>
<span data-ttu-id="64275-165">Anger namnet på platsen där moln tjänsten är värd.</span><span class="sxs-lookup"><span data-stu-id="64275-165">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="64275-166">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="64275-166">Valid values are:</span></span> 

- <span data-ttu-id="64275-167">Världen över</span><span class="sxs-lookup"><span data-stu-id="64275-167">Anywhere Asia</span></span>
- <span data-ttu-id="64275-168">Överallt i Europa</span><span class="sxs-lookup"><span data-stu-id="64275-168">Anywhere Europe</span></span>
- <span data-ttu-id="64275-169">Var du än är</span><span class="sxs-lookup"><span data-stu-id="64275-169">Anywhere US</span></span>
- <span data-ttu-id="64275-170">Östasien</span><span class="sxs-lookup"><span data-stu-id="64275-170">East Asia</span></span>
- <span data-ttu-id="64275-171">Östra USA</span><span class="sxs-lookup"><span data-stu-id="64275-171">East US</span></span>
- <span data-ttu-id="64275-172">Norra Central USA</span><span class="sxs-lookup"><span data-stu-id="64275-172">North Central US</span></span>
- <span data-ttu-id="64275-173">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="64275-173">North Europe</span></span>
- <span data-ttu-id="64275-174">Södra centrala USA</span><span class="sxs-lookup"><span data-stu-id="64275-174">South Central US</span></span>
- <span data-ttu-id="64275-175">Sydostasien</span><span class="sxs-lookup"><span data-stu-id="64275-175">Southeast Asia</span></span>
- <span data-ttu-id="64275-176">Västeuropa</span><span class="sxs-lookup"><span data-stu-id="64275-176">West Europe</span></span>
- <span data-ttu-id="64275-177">Västra USA</span><span class="sxs-lookup"><span data-stu-id="64275-177">West US</span></span>

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

### <span data-ttu-id="64275-178">-Metod</span><span class="sxs-lookup"><span data-stu-id="64275-178">-Method</span></span>
<span data-ttu-id="64275-179">Anger metod för HTTP-och HTTPS-åtgärds typer.</span><span class="sxs-lookup"><span data-stu-id="64275-179">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="64275-180">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="64275-180">Valid values are:</span></span> 

- <span data-ttu-id="64275-181">LÄRA</span><span class="sxs-lookup"><span data-stu-id="64275-181">GET</span></span>
- <span data-ttu-id="64275-182">ÖRSEL</span><span class="sxs-lookup"><span data-stu-id="64275-182">PUT</span></span>
- <span data-ttu-id="64275-183">TEST</span><span class="sxs-lookup"><span data-stu-id="64275-183">POST</span></span>
- <span data-ttu-id="64275-184">HUVUDEN</span><span class="sxs-lookup"><span data-stu-id="64275-184">HEAD</span></span>
- <span data-ttu-id="64275-185">TA bort</span><span class="sxs-lookup"><span data-stu-id="64275-185">DELETE</span></span>

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

### <span data-ttu-id="64275-186">-PassThru</span><span class="sxs-lookup"><span data-stu-id="64275-186">-PassThru</span></span>
<span data-ttu-id="64275-187">Anger att den här cmdleten returnerar ett objekt som representerar det objekt som den körs på.</span><span class="sxs-lookup"><span data-stu-id="64275-187">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="64275-188">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="64275-188">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="64275-189">-Profil</span><span class="sxs-lookup"><span data-stu-id="64275-189">-Profile</span></span>
<span data-ttu-id="64275-190">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="64275-190">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="64275-191">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="64275-191">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="64275-192">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="64275-192">-RequestBody</span></span>
<span data-ttu-id="64275-193">Anger brödtext för att placera och BOKFÖRA jobb åtgärder.</span><span class="sxs-lookup"><span data-stu-id="64275-193">Specifies the body for PUT and POST job actions.</span></span>

```yaml
Type: String
Parameter Sets: Required, PutPost
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64275-194">-StartTime</span><span class="sxs-lookup"><span data-stu-id="64275-194">-StartTime</span></span>
<span data-ttu-id="64275-195">Anger ett klock slag, som ett **datetime** -objekt, för jobbet som ska starta.</span><span class="sxs-lookup"><span data-stu-id="64275-195">Specifies a time, as a **DateTime** object, for the job to start.</span></span>

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

### <span data-ttu-id="64275-196">-URI</span><span class="sxs-lookup"><span data-stu-id="64275-196">-URI</span></span>
<span data-ttu-id="64275-197">Anger en URI för en jobb åtgärd.</span><span class="sxs-lookup"><span data-stu-id="64275-197">Specifies a URI for a job action.</span></span>

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

### <span data-ttu-id="64275-198">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64275-198">CommonParameters</span></span>
<span data-ttu-id="64275-199">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64275-199">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64275-200">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64275-200">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64275-201">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="64275-201">INPUTS</span></span>

## <span data-ttu-id="64275-202">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="64275-202">OUTPUTS</span></span>

## <span data-ttu-id="64275-203">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="64275-203">NOTES</span></span>

## <span data-ttu-id="64275-204">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="64275-204">RELATED LINKS</span></span>

[<span data-ttu-id="64275-205">New-AzureSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="64275-205">New-AzureSchedulerHttpJob</span></span>](./New-AzureSchedulerHttpJob.md)


