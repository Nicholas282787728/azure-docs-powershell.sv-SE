---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 31F2AF24-488D-4CAF-A9C8-C8DAE76E031F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyDefinition.md
ms.openlocfilehash: e39d60863b9409a6d52f2f92dc312e98b8e50cf9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575535"
---
# <span data-ttu-id="d582e-101">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d582e-101">New-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="d582e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d582e-102">SYNOPSIS</span></span>
<span data-ttu-id="d582e-103">Skapar en princip definition.</span><span class="sxs-lookup"><span data-stu-id="d582e-103">Creates a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d582e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d582e-104">SYNTAX</span></span>

```
New-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d582e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d582e-105">DESCRIPTION</span></span>
<span data-ttu-id="d582e-106">Cmdleten **New-AzureRmPolicyDefinition** skapar en princip definition som innehåller en policy regel i JSON-format (Java Object Notation).</span><span class="sxs-lookup"><span data-stu-id="d582e-106">The **New-AzureRmPolicyDefinition** cmdlet creates a policy definition that includes a policy rule in JavaScript Object Notation (JSON) format.</span></span>

## <span data-ttu-id="d582e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d582e-107">EXAMPLES</span></span>

### <span data-ttu-id="d582e-108">Exempel 1: skapa en princip definition med hjälp av en princip fil</span><span class="sxs-lookup"><span data-stu-id="d582e-108">Example 1: Create a policy definition by using a policy file</span></span>
```
PS C:\>New-AzureRmPolicyDefinition -Name "VMPolicyDefinition" -Policy C:\VMPolicy.json
```

<span data-ttu-id="d582e-109">Det här kommandot skapar en princip definition med namnet VMPolicyDefinition som innehåller policy regeln som angetts i C:\VMPolicy.js.</span><span class="sxs-lookup"><span data-stu-id="d582e-109">This command creates a policy definition named VMPolicyDefinition that contains the policy rule specified in C:\VMPolicy.json.</span></span>

### <span data-ttu-id="d582e-110">Exempel 2: skapa en rad i princip definitionen</span><span class="sxs-lookup"><span data-stu-id="d582e-110">Example 2: Create a policy definition inline</span></span>
```
PS C:\>New-AzureRmPolicyDefinition -Name "VMPolicyDefinition" -DisplayName "Virtual Machine policy definition" -Policy "{""if"":{""source"":""action"",""equals"":""Microsoft.Compute/virtualMachines/write""},""then"":{""effect"":""deny""}}"
```

<span data-ttu-id="d582e-111">Det här kommandot skapar en princip definition med namnet VMPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="d582e-111">This command creates a policy definition named VMPolicyDefinition.</span></span>
<span data-ttu-id="d582e-112">Kommandot anger principen som en sträng i giltigt JSON-format.</span><span class="sxs-lookup"><span data-stu-id="d582e-112">The command specifies the policy as a string in valid JSON format.</span></span>

## <span data-ttu-id="d582e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d582e-113">PARAMETERS</span></span>

### <span data-ttu-id="d582e-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d582e-114">-ApiVersion</span></span>
<span data-ttu-id="d582e-115">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="d582e-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="d582e-116">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="d582e-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="d582e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d582e-117">-DefaultProfile</span></span>
<span data-ttu-id="d582e-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d582e-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d582e-119">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="d582e-119">-Description</span></span>
<span data-ttu-id="d582e-120">Anger en beskrivning för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="d582e-120">Specifies a description for the policy definition.</span></span>

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

### <span data-ttu-id="d582e-121">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d582e-121">-DisplayName</span></span>
<span data-ttu-id="d582e-122">Anger ett visnings namn för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="d582e-122">Specifies a display name for the policy definition.</span></span>

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

### <span data-ttu-id="d582e-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d582e-123">-InformationAction</span></span>
<span data-ttu-id="d582e-124">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="d582e-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d582e-125">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="d582e-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d582e-126">Vidare</span><span class="sxs-lookup"><span data-stu-id="d582e-126">Continue</span></span>
- <span data-ttu-id="d582e-127">Över</span><span class="sxs-lookup"><span data-stu-id="d582e-127">Ignore</span></span>
- <span data-ttu-id="d582e-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="d582e-128">Inquire</span></span>
- <span data-ttu-id="d582e-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d582e-129">SilentlyContinue</span></span>
- <span data-ttu-id="d582e-130">Stanna</span><span class="sxs-lookup"><span data-stu-id="d582e-130">Stop</span></span>
- <span data-ttu-id="d582e-131">Avbryt</span><span class="sxs-lookup"><span data-stu-id="d582e-131">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d582e-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d582e-132">-InformationVariable</span></span>
<span data-ttu-id="d582e-133">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="d582e-133">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d582e-134">-Metadata</span><span class="sxs-lookup"><span data-stu-id="d582e-134">-Metadata</span></span>
<span data-ttu-id="d582e-135">Metadata för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="d582e-135">The metadata for policy definition.</span></span> <span data-ttu-id="d582e-136">Det kan antingen vara en sökväg till ett fil namn som innehåller metadata, eller metadata som sträng</span><span class="sxs-lookup"><span data-stu-id="d582e-136">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="d582e-137">-Mode</span><span class="sxs-lookup"><span data-stu-id="d582e-137">-Mode</span></span>
<span data-ttu-id="d582e-138">Läget för princip definitionen</span><span class="sxs-lookup"><span data-stu-id="d582e-138">The mode of the policy definition</span></span>

```yaml
Type: PolicyDefinitionMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d582e-139">-Namn</span><span class="sxs-lookup"><span data-stu-id="d582e-139">-Name</span></span>
<span data-ttu-id="d582e-140">Anger ett namn för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="d582e-140">Specifies a name for the policy definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d582e-141">-Parameter</span><span class="sxs-lookup"><span data-stu-id="d582e-141">-Parameter</span></span>
<span data-ttu-id="d582e-142">Parameter deklarationen för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="d582e-142">The parameters declaration for policy definition.</span></span> <span data-ttu-id="d582e-143">Det kan antingen vara en sökväg till ett fil namn som innehåller parameter deklarationen eller parameter deklarationen som sträng.</span><span class="sxs-lookup"><span data-stu-id="d582e-143">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="d582e-144">-Princip</span><span class="sxs-lookup"><span data-stu-id="d582e-144">-Policy</span></span>
<span data-ttu-id="d582e-145">Anger en policy regel för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="d582e-145">Specifies a policy rule for the policy definition.</span></span>
<span data-ttu-id="d582e-146">Du kan ange sökvägen till en. JSON-fil eller en sträng som innehåller principen i JSON-format.</span><span class="sxs-lookup"><span data-stu-id="d582e-146">You can specify the path of a .json file or a string that contains the policy in JSON format.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d582e-147">-För</span><span class="sxs-lookup"><span data-stu-id="d582e-147">-Pre</span></span>
<span data-ttu-id="d582e-148">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="d582e-148">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="d582e-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d582e-149">CommonParameters</span></span>
<span data-ttu-id="d582e-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d582e-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d582e-151">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d582e-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d582e-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d582e-152">INPUTS</span></span>

### <span data-ttu-id="d582e-153">Ingen</span><span class="sxs-lookup"><span data-stu-id="d582e-153">None</span></span>
<span data-ttu-id="d582e-154">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="d582e-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d582e-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d582e-155">OUTPUTS</span></span>

### <span data-ttu-id="d582e-156">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="d582e-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="d582e-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d582e-157">NOTES</span></span>

## <span data-ttu-id="d582e-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d582e-158">RELATED LINKS</span></span>

[<span data-ttu-id="d582e-159">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d582e-159">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="d582e-160">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d582e-160">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="d582e-161">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d582e-161">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


