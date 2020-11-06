---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 31F2AF24-488D-4CAF-A9C8-C8DAE76E031F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyDefinition.md
ms.openlocfilehash: 5140219c5392a7fb9c727998ae248d600edfde23
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582220"
---
# <span data-ttu-id="76f91-101">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="76f91-101">New-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="76f91-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="76f91-102">SYNOPSIS</span></span>
<span data-ttu-id="76f91-103">Skapar en princip definition.</span><span class="sxs-lookup"><span data-stu-id="76f91-103">Creates a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76f91-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="76f91-104">SYNTAX</span></span>

```
New-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="76f91-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="76f91-105">DESCRIPTION</span></span>
<span data-ttu-id="76f91-106">Cmdleten **New-AzureRmPolicyDefinition** skapar en princip definition som innehåller en policy regel i JSON-format (Java Object Notation).</span><span class="sxs-lookup"><span data-stu-id="76f91-106">The **New-AzureRmPolicyDefinition** cmdlet creates a policy definition that includes a policy rule in JavaScript Object Notation (JSON) format.</span></span>

## <span data-ttu-id="76f91-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="76f91-107">EXAMPLES</span></span>

### <span data-ttu-id="76f91-108">Exempel 1: skapa en princip definition med hjälp av en princip fil</span><span class="sxs-lookup"><span data-stu-id="76f91-108">Example 1: Create a policy definition by using a policy file</span></span>
```
PS C:\>New-AzureRmPolicyDefinition -Name "VMPolicyDefinition" -Policy C:\VMPolicy.json
```

<span data-ttu-id="76f91-109">Det här kommandot skapar en princip definition med namnet VMPolicyDefinition som innehåller policy regeln som angetts i C:\VMPolicy.js.</span><span class="sxs-lookup"><span data-stu-id="76f91-109">This command creates a policy definition named VMPolicyDefinition that contains the policy rule specified in C:\VMPolicy.json.</span></span>

### <span data-ttu-id="76f91-110">Exempel 2: skapa en rad i princip definitionen</span><span class="sxs-lookup"><span data-stu-id="76f91-110">Example 2: Create a policy definition inline</span></span>
```
PS C:\>New-AzureRmPolicyDefinition -Name "VMPolicyDefinition" -DisplayName "Virtual Machine policy definition" -Policy "{""if"":{""source"":""action"",""equals"":""Microsoft.Compute/virtualMachines/write""},""then"":{""effect"":""deny""}}"
```

<span data-ttu-id="76f91-111">Det här kommandot skapar en princip definition med namnet VMPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="76f91-111">This command creates a policy definition named VMPolicyDefinition.</span></span>
<span data-ttu-id="76f91-112">Kommandot anger principen som en sträng i giltigt JSON-format.</span><span class="sxs-lookup"><span data-stu-id="76f91-112">The command specifies the policy as a string in valid JSON format.</span></span>

## <span data-ttu-id="76f91-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="76f91-113">PARAMETERS</span></span>

### <span data-ttu-id="76f91-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="76f91-114">-ApiVersion</span></span>
<span data-ttu-id="76f91-115">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="76f91-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="76f91-116">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="76f91-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76f91-117">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="76f91-117">-Description</span></span>
<span data-ttu-id="76f91-118">Anger en beskrivning för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="76f91-118">Specifies a description for the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76f91-119">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="76f91-119">-DisplayName</span></span>
<span data-ttu-id="76f91-120">Anger ett visnings namn för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="76f91-120">Specifies a display name for the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76f91-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="76f91-121">-InformationAction</span></span>
<span data-ttu-id="76f91-122">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="76f91-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="76f91-123">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="76f91-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="76f91-124">Vidare</span><span class="sxs-lookup"><span data-stu-id="76f91-124">Continue</span></span>
- <span data-ttu-id="76f91-125">Över</span><span class="sxs-lookup"><span data-stu-id="76f91-125">Ignore</span></span>
- <span data-ttu-id="76f91-126">Inquire</span><span class="sxs-lookup"><span data-stu-id="76f91-126">Inquire</span></span>
- <span data-ttu-id="76f91-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="76f91-127">SilentlyContinue</span></span>
- <span data-ttu-id="76f91-128">Stanna</span><span class="sxs-lookup"><span data-stu-id="76f91-128">Stop</span></span>
- <span data-ttu-id="76f91-129">Avbryt</span><span class="sxs-lookup"><span data-stu-id="76f91-129">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76f91-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="76f91-130">-InformationVariable</span></span>
<span data-ttu-id="76f91-131">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="76f91-131">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76f91-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="76f91-132">-Name</span></span>
<span data-ttu-id="76f91-133">Anger ett namn för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="76f91-133">Specifies a name for the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76f91-134">-Parameter</span><span class="sxs-lookup"><span data-stu-id="76f91-134">-Parameter</span></span>
<span data-ttu-id="76f91-135">Parameter deklarationen för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="76f91-135">The parameters declaration for policy definition.</span></span> <span data-ttu-id="76f91-136">Det kan antingen vara en sökväg till ett fil namn som innehåller parameter deklarationen eller parameter deklarationen som sträng.</span><span class="sxs-lookup"><span data-stu-id="76f91-136">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76f91-137">-Princip</span><span class="sxs-lookup"><span data-stu-id="76f91-137">-Policy</span></span>
<span data-ttu-id="76f91-138">Anger en policy regel för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="76f91-138">Specifies a policy rule for the policy definition.</span></span>
<span data-ttu-id="76f91-139">Du kan ange sökvägen till en. JSON-fil eller en sträng som innehåller principen i JSON-format.</span><span class="sxs-lookup"><span data-stu-id="76f91-139">You can specify the path of a .json file or a string that contains the policy in JSON format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76f91-140">-För</span><span class="sxs-lookup"><span data-stu-id="76f91-140">-Pre</span></span>
<span data-ttu-id="76f91-141">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="76f91-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76f91-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76f91-142">-DefaultProfile</span></span>
<span data-ttu-id="76f91-143">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="76f91-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76f91-144">-Metadata</span><span class="sxs-lookup"><span data-stu-id="76f91-144">-Metadata</span></span>
<span data-ttu-id="76f91-145">Metadata för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="76f91-145">The metadata for policy definition.</span></span> <span data-ttu-id="76f91-146">Det kan antingen vara en sökväg till ett fil namn som innehåller metadata eller metadata som sträng.</span><span class="sxs-lookup"><span data-stu-id="76f91-146">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76f91-147">-Mode</span><span class="sxs-lookup"><span data-stu-id="76f91-147">-Mode</span></span>
<span data-ttu-id="76f91-148">Läget för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="76f91-148">The mode of the policy definition.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Policy.PolicyDefinitionMode]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76f91-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76f91-149">CommonParameters</span></span>
<span data-ttu-id="76f91-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76f91-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76f91-151">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76f91-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76f91-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="76f91-152">INPUTS</span></span>

## <span data-ttu-id="76f91-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="76f91-153">OUTPUTS</span></span>

### <span data-ttu-id="76f91-154">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="76f91-154">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="76f91-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="76f91-155">NOTES</span></span>

## <span data-ttu-id="76f91-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="76f91-156">RELATED LINKS</span></span>

[<span data-ttu-id="76f91-157">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="76f91-157">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="76f91-158">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="76f91-158">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="76f91-159">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="76f91-159">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


