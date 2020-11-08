---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: C608BBDD-DC2B-4BEF-812D-0BAE94FB4395
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0f5332c18d2d47096f246485ac0d811548f70aa9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099134"
---
# <span data-ttu-id="69885-101">New-AzureSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="69885-101">New-AzureSchedulerHttpJob</span></span>

## <span data-ttu-id="69885-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="69885-102">SYNOPSIS</span></span>
<span data-ttu-id="69885-103">Skapar ett jobb i schemaläggare med en HTTP-åtgärd.</span><span class="sxs-lookup"><span data-stu-id="69885-103">Creates a scheduler job that has an HTTP action.</span></span>

## <span data-ttu-id="69885-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="69885-104">SYNTAX</span></span>

### <span data-ttu-id="69885-105">Kunna</span><span class="sxs-lookup"><span data-stu-id="69885-105">Required</span></span>
```
New-AzureSchedulerHttpJob -Location <String> -JobCollectionName <String> -JobName <String> -Method <String>
 -URI <Uri> [-RequestBody <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-ExecutionCount <Int32>] [-EndTime <DateTime>] [-JobState <String>] [-Headers <Hashtable>]
 [-ErrorActionMethod <String>] [-ErrorActionURI <Uri>] [-ErrorActionRequestBody <String>]
 [-ErrorActionHeaders <Hashtable>] [-ErrorActionStorageAccount <String>] [-ErrorActionStorageQueue <String>]
 [-ErrorActionSASToken <String>] [-ErrorActionQueueMessageBody <String>] [-HttpAuthenticationType <String>]
 [-ClientCertificatePfx <Object>] [-ClientCertificatePassword <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="69885-106">PutPost</span><span class="sxs-lookup"><span data-stu-id="69885-106">PutPost</span></span>
```
New-AzureSchedulerHttpJob [-RequestBody <String>] [-JobState <String>] [-Headers <Hashtable>]
 [-ErrorActionHeaders <Hashtable>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="69885-107">Kommer</span><span class="sxs-lookup"><span data-stu-id="69885-107">Recurring</span></span>
```
New-AzureSchedulerHttpJob [-Interval <Int32>] [-Frequency <String>] [-ExecutionCount <Int32>]
 [-EndTime <DateTime>] [-JobState <String>] [-Headers <Hashtable>] [-ErrorActionHeaders <Hashtable>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="69885-108">Verifieringsmetoden</span><span class="sxs-lookup"><span data-stu-id="69885-108">Authentication</span></span>
```
New-AzureSchedulerHttpJob [-JobState <String>] [-Headers <Hashtable>] [-ErrorActionHeaders <Hashtable>]
 -HttpAuthenticationType <String> [-ClientCertificatePfx <Object>] [-ClientCertificatePassword <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="69885-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="69885-109">DESCRIPTION</span></span>
<span data-ttu-id="69885-110">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="69885-110">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="69885-111">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="69885-111">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="69885-112">Cmdleten **New-AzureSchedulerHttpJob** skapar ett jobb i schemaläggare som har en HTTP-åtgärd.</span><span class="sxs-lookup"><span data-stu-id="69885-112">The **New-AzureSchedulerHttpJob** cmdlet creates a scheduler job that has an HTTP action.</span></span>

## <span data-ttu-id="69885-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="69885-113">EXAMPLES</span></span>

### <span data-ttu-id="69885-114">Exempel 1: skapa ett HTTP-jobb</span><span class="sxs-lookup"><span data-stu-id="69885-114">Example 1: Create an HTTP job</span></span>
```
PS C:\> New-AzureSchedulerHttpJob -JobCollectionName "JobCollection01" -JobName "Job01" -Location "North Central US" -Method "GET" -URI http://www.contoso.com
```

<span data-ttu-id="69885-115">Det här kommandot skapar ett HTTP-jobb för Schemaläggaren i jobb samlingen med namnet JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="69885-115">This command creates a scheduler HTTP job in the job collection named JobCollection01.</span></span>
<span data-ttu-id="69885-116">Kommandot anger en URI och anger GET som metod.</span><span class="sxs-lookup"><span data-stu-id="69885-116">The command specifies a URI and specifies GET as the method.</span></span>

### <span data-ttu-id="69885-117">Exempel 2: skapa ett HTTP-jobb för ett visst antal körningar</span><span class="sxs-lookup"><span data-stu-id="69885-117">Example 2: Create an HTTP job for a specific run count</span></span>
```
PS C:\> New-AzureSchedulerHttpJob -JobCollectionName "JobCollection01 -JobName "Job23" -Location "North Central US" -Method "GET" -URI http://www.contoso.com -ExecutionCount 20
```

<span data-ttu-id="69885-118">Det här kommandot skapar Schemaläggarens http-jobb i jobb samlingen med namnet JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="69885-118">This command creates scheduler http job in the job collection named JobCollection01.</span></span>
<span data-ttu-id="69885-119">Kommandot anger en URI och anger GET som metod.</span><span class="sxs-lookup"><span data-stu-id="69885-119">The command specifies a URI and specifies GET as the method.</span></span>
<span data-ttu-id="69885-120">Detta kommando gör att jobbet körs 20 gånger.</span><span class="sxs-lookup"><span data-stu-id="69885-120">This command causes the job to run 20 times.</span></span>

## <span data-ttu-id="69885-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="69885-121">PARAMETERS</span></span>

### <span data-ttu-id="69885-122">-ClientCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="69885-122">-ClientCertificatePassword</span></span>
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

### <span data-ttu-id="69885-123">-ClientCertificatePfx</span><span class="sxs-lookup"><span data-stu-id="69885-123">-ClientCertificatePfx</span></span>
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

### <span data-ttu-id="69885-124">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="69885-124">-EndTime</span></span>
<span data-ttu-id="69885-125">Anger ett klock slag, som ett **datetime** -objekt, för Schemaläggaren att sluta initiera jobb.</span><span class="sxs-lookup"><span data-stu-id="69885-125">Specifies a time, as a **DateTime** object, for the scheduler to stop initiating jobs.</span></span>
<span data-ttu-id="69885-126">Använd cmdleten **Get-date** för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="69885-126">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="69885-127">Om du vill ha mer information skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="69885-127">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="69885-128">-ErrorActionHeaders</span><span class="sxs-lookup"><span data-stu-id="69885-128">-ErrorActionHeaders</span></span>
<span data-ttu-id="69885-129">Anger rubriker som en hash-gruppnamn.</span><span class="sxs-lookup"><span data-stu-id="69885-129">Specifies headers as a hashtable.</span></span>

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

### <span data-ttu-id="69885-130">-ErrorActionMethod</span><span class="sxs-lookup"><span data-stu-id="69885-130">-ErrorActionMethod</span></span>
<span data-ttu-id="69885-131">Anger metod för HTTP-och HTTPS-åtgärds typer.</span><span class="sxs-lookup"><span data-stu-id="69885-131">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="69885-132">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="69885-132">Valid values are:</span></span> 

- <span data-ttu-id="69885-133">LÄRA</span><span class="sxs-lookup"><span data-stu-id="69885-133">GET</span></span>
- <span data-ttu-id="69885-134">ÖRSEL</span><span class="sxs-lookup"><span data-stu-id="69885-134">PUT</span></span>
- <span data-ttu-id="69885-135">TEST</span><span class="sxs-lookup"><span data-stu-id="69885-135">POST</span></span>
- <span data-ttu-id="69885-136">HUVUDEN</span><span class="sxs-lookup"><span data-stu-id="69885-136">HEAD</span></span>
- <span data-ttu-id="69885-137">TA bort</span><span class="sxs-lookup"><span data-stu-id="69885-137">DELETE</span></span>

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

### <span data-ttu-id="69885-138">-ErrorActionQueueMessageBody</span><span class="sxs-lookup"><span data-stu-id="69885-138">-ErrorActionQueueMessageBody</span></span>
<span data-ttu-id="69885-139">Anger bröd texten för lagrings jobb åtgärder.</span><span class="sxs-lookup"><span data-stu-id="69885-139">Specifies the body for storage job actions.</span></span>

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

### <span data-ttu-id="69885-140">-ErrorActionRequestBody</span><span class="sxs-lookup"><span data-stu-id="69885-140">-ErrorActionRequestBody</span></span>
<span data-ttu-id="69885-141">Anger brödtext för att placera och BOKFÖRA jobb åtgärder.</span><span class="sxs-lookup"><span data-stu-id="69885-141">Specifies the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="69885-142">-ErrorActionSASToken</span><span class="sxs-lookup"><span data-stu-id="69885-142">-ErrorActionSASToken</span></span>
<span data-ttu-id="69885-143">Anger den delade Access-signaturen (SAS) för lagrings kön.</span><span class="sxs-lookup"><span data-stu-id="69885-143">Specifies the Shared Access Signature (SAS) token for the storage queue.</span></span>

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

### <span data-ttu-id="69885-144">-ErrorActionStorageAccount</span><span class="sxs-lookup"><span data-stu-id="69885-144">-ErrorActionStorageAccount</span></span>
<span data-ttu-id="69885-145">Anger namnet på lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="69885-145">Specifies the name of the storage account.</span></span>

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

### <span data-ttu-id="69885-146">-ErrorActionStorageQueue</span><span class="sxs-lookup"><span data-stu-id="69885-146">-ErrorActionStorageQueue</span></span>
<span data-ttu-id="69885-147">Anger namnet på lagrings kön.</span><span class="sxs-lookup"><span data-stu-id="69885-147">Specifies the name of the storage queue.</span></span>

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

### <span data-ttu-id="69885-148">-ErrorActionURI</span><span class="sxs-lookup"><span data-stu-id="69885-148">-ErrorActionURI</span></span>
<span data-ttu-id="69885-149">Anger URI för fel åtgärds åtgärden.</span><span class="sxs-lookup"><span data-stu-id="69885-149">Specifies the URI for the error job action.</span></span>

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

### <span data-ttu-id="69885-150">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="69885-150">-ExecutionCount</span></span>
<span data-ttu-id="69885-151">Anger antalet förekomster av ett jobb som körs.</span><span class="sxs-lookup"><span data-stu-id="69885-151">Specifies the number occurrences of a job that run.</span></span>
<span data-ttu-id="69885-152">Vanligt vis returnerar ett jobb oändligt.</span><span class="sxs-lookup"><span data-stu-id="69885-152">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="69885-153">-Frekvens</span><span class="sxs-lookup"><span data-stu-id="69885-153">-Frequency</span></span>
<span data-ttu-id="69885-154">Anger den maximala frekvensen för det här Schemaläggaren-jobbet.</span><span class="sxs-lookup"><span data-stu-id="69885-154">Specifies the maximum frequency for this scheduler job.</span></span>

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

### <span data-ttu-id="69885-155">-Rubriker</span><span class="sxs-lookup"><span data-stu-id="69885-155">-Headers</span></span>
<span data-ttu-id="69885-156">Anger rubriker som en hash-tabellen.</span><span class="sxs-lookup"><span data-stu-id="69885-156">Specifies the headers as a hashtable.</span></span>

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

### <span data-ttu-id="69885-157">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="69885-157">-HttpAuthenticationType</span></span>
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

### <span data-ttu-id="69885-158">-Intervall</span><span class="sxs-lookup"><span data-stu-id="69885-158">-Interval</span></span>
<span data-ttu-id="69885-159">Anger upprepnings intervallet för frekvensen som anges med hjälp av parametern *frekvens* .</span><span class="sxs-lookup"><span data-stu-id="69885-159">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

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

### <span data-ttu-id="69885-160">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="69885-160">-JobCollectionName</span></span>
<span data-ttu-id="69885-161">Anger namnet på den samling som ska innehålla jobbet schemaläggare.</span><span class="sxs-lookup"><span data-stu-id="69885-161">Specifies the name of the collection to contain the scheduler job.</span></span>

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

### <span data-ttu-id="69885-162">-JobName</span><span class="sxs-lookup"><span data-stu-id="69885-162">-JobName</span></span>
<span data-ttu-id="69885-163">Anger namnet på jobbet i Schemaläggaren.</span><span class="sxs-lookup"><span data-stu-id="69885-163">Specifies the name for the scheduler job.</span></span>

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

### <span data-ttu-id="69885-164">-JobState</span><span class="sxs-lookup"><span data-stu-id="69885-164">-JobState</span></span>
<span data-ttu-id="69885-165">Anger tillstånd för jobb i schemaläggare.</span><span class="sxs-lookup"><span data-stu-id="69885-165">Specifies the state for the scheduler job.</span></span>

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

### <span data-ttu-id="69885-166">-Plats</span><span class="sxs-lookup"><span data-stu-id="69885-166">-Location</span></span>
<span data-ttu-id="69885-167">Anger namnet på platsen där moln tjänsten är värd.</span><span class="sxs-lookup"><span data-stu-id="69885-167">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="69885-168">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="69885-168">Valid values are:</span></span> 

- <span data-ttu-id="69885-169">Världen över</span><span class="sxs-lookup"><span data-stu-id="69885-169">Anywhere Asia</span></span>
- <span data-ttu-id="69885-170">Överallt i Europa</span><span class="sxs-lookup"><span data-stu-id="69885-170">Anywhere Europe</span></span>
- <span data-ttu-id="69885-171">Var du än är</span><span class="sxs-lookup"><span data-stu-id="69885-171">Anywhere US</span></span>
- <span data-ttu-id="69885-172">Östasien</span><span class="sxs-lookup"><span data-stu-id="69885-172">East Asia</span></span>
- <span data-ttu-id="69885-173">Östra USA</span><span class="sxs-lookup"><span data-stu-id="69885-173">East US</span></span>
- <span data-ttu-id="69885-174">Norra Central USA</span><span class="sxs-lookup"><span data-stu-id="69885-174">North Central US</span></span>
- <span data-ttu-id="69885-175">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="69885-175">North Europe</span></span>
- <span data-ttu-id="69885-176">Södra centrala USA</span><span class="sxs-lookup"><span data-stu-id="69885-176">South Central US</span></span>
- <span data-ttu-id="69885-177">Sydostasien</span><span class="sxs-lookup"><span data-stu-id="69885-177">Southeast Asia</span></span>
- <span data-ttu-id="69885-178">Västeuropa</span><span class="sxs-lookup"><span data-stu-id="69885-178">West Europe</span></span>
- <span data-ttu-id="69885-179">Västra USA</span><span class="sxs-lookup"><span data-stu-id="69885-179">West US</span></span>

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

### <span data-ttu-id="69885-180">-Metod</span><span class="sxs-lookup"><span data-stu-id="69885-180">-Method</span></span>
<span data-ttu-id="69885-181">Anger metod för HTTP-och HTTPS-åtgärds typer.</span><span class="sxs-lookup"><span data-stu-id="69885-181">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="69885-182">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="69885-182">Valid values are:</span></span> 

- <span data-ttu-id="69885-183">LÄRA</span><span class="sxs-lookup"><span data-stu-id="69885-183">GET</span></span>
- <span data-ttu-id="69885-184">ÖRSEL</span><span class="sxs-lookup"><span data-stu-id="69885-184">PUT</span></span>
- <span data-ttu-id="69885-185">TEST</span><span class="sxs-lookup"><span data-stu-id="69885-185">POST</span></span>
- <span data-ttu-id="69885-186">HUVUDEN</span><span class="sxs-lookup"><span data-stu-id="69885-186">HEAD</span></span>
- <span data-ttu-id="69885-187">TA bort</span><span class="sxs-lookup"><span data-stu-id="69885-187">DELETE</span></span>

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

### <span data-ttu-id="69885-188">-Profil</span><span class="sxs-lookup"><span data-stu-id="69885-188">-Profile</span></span>
<span data-ttu-id="69885-189">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="69885-189">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="69885-190">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="69885-190">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="69885-191">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="69885-191">-RequestBody</span></span>
<span data-ttu-id="69885-192">Anger brödtext för att placera och BOKFÖRA jobb åtgärder.</span><span class="sxs-lookup"><span data-stu-id="69885-192">Specifies the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="69885-193">-StartTime</span><span class="sxs-lookup"><span data-stu-id="69885-193">-StartTime</span></span>
<span data-ttu-id="69885-194">Anger ett klock slag, som ett **datetime** -objekt, för jobbet som ska starta.</span><span class="sxs-lookup"><span data-stu-id="69885-194">Specifies a time, as a **DateTime** object, for the job to start.</span></span>

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

### <span data-ttu-id="69885-195">-URI</span><span class="sxs-lookup"><span data-stu-id="69885-195">-URI</span></span>
<span data-ttu-id="69885-196">Anger en URI för en jobb åtgärd.</span><span class="sxs-lookup"><span data-stu-id="69885-196">Specifies a URI for a job action.</span></span>

```yaml
Type: Uri
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69885-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69885-197">CommonParameters</span></span>
<span data-ttu-id="69885-198">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69885-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69885-199">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69885-199">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69885-200">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="69885-200">INPUTS</span></span>

## <span data-ttu-id="69885-201">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="69885-201">OUTPUTS</span></span>

## <span data-ttu-id="69885-202">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="69885-202">NOTES</span></span>

## <span data-ttu-id="69885-203">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="69885-203">RELATED LINKS</span></span>

[<span data-ttu-id="69885-204">Set-AzureSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="69885-204">Set-AzureSchedulerHttpJob</span></span>](./Set-AzureSchedulerHttpJob.md)


