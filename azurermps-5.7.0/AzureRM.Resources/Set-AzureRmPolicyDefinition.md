---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyDefinition.md
ms.openlocfilehash: d7e01294836145b09844fa3bca49421df20f67d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581984"
---
# <span data-ttu-id="4226f-101">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4226f-101">Set-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="4226f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4226f-102">SYNOPSIS</span></span>
<span data-ttu-id="4226f-103">Ändrar en princip definition.</span><span class="sxs-lookup"><span data-stu-id="4226f-103">Modifies a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4226f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4226f-104">SYNTAX</span></span>

### <span data-ttu-id="4226f-105">SetByPolicyDefinitionName (standard)</span><span class="sxs-lookup"><span data-stu-id="4226f-105">SetByPolicyDefinitionName (Default)</span></span>
```
Set-AzureRmPolicyDefinition [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="4226f-106">GetByPolicyDefintionName</span><span class="sxs-lookup"><span data-stu-id="4226f-106">GetByPolicyDefintionName</span></span>
```
Set-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="4226f-107">GetByPolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="4226f-107">GetByPolicyDefinitionId</span></span>
```
Set-AzureRmPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="4226f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4226f-108">DESCRIPTION</span></span>
<span data-ttu-id="4226f-109">Cmdleten **set-AzureRmPolicyDefinition** ändrar en princip definition.</span><span class="sxs-lookup"><span data-stu-id="4226f-109">The **Set-AzureRmPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="4226f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4226f-110">EXAMPLES</span></span>

### <span data-ttu-id="4226f-111">Exempel 1: Uppdatera beskrivningen av en princip definition</span><span class="sxs-lookup"><span data-stu-id="4226f-111">Example 1: Update the description of a policy definition</span></span>
```
PS C:\>$PolicyDefinition = Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
PS C:\> Set-AzureRmPolicyDefinition -Id $Policy.ResourceId -Description "Updated policy to not allow virtual machine creation"
```

<span data-ttu-id="4226f-112">Det första kommandot hämtar princip definitionen med namnet VMPolicyDefinition med hjälp av Get-AzureRmPolicyDefinition cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4226f-112">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="4226f-113">Kommandot lagrar objektet i $PolicyDefinition variabel.</span><span class="sxs-lookup"><span data-stu-id="4226f-113">The command stores that object in the $PolicyDefinition variable.</span></span>

<span data-ttu-id="4226f-114">Det andra kommandot uppdaterar beskrivningen av princip definitionen som identifieras av egenskapen **ResourceID** för $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="4226f-114">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="4226f-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4226f-115">PARAMETERS</span></span>

### <span data-ttu-id="4226f-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4226f-116">-ApiVersion</span></span>
<span data-ttu-id="4226f-117">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="4226f-117">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="4226f-118">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="4226f-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="4226f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4226f-119">-DefaultProfile</span></span>
<span data-ttu-id="4226f-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="4226f-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4226f-121">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="4226f-121">-Description</span></span>
<span data-ttu-id="4226f-122">Anger en ny beskrivning för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="4226f-122">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="4226f-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4226f-123">-DisplayName</span></span>
<span data-ttu-id="4226f-124">Anger ett nytt visnings namn för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="4226f-124">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="4226f-125">-ID</span><span class="sxs-lookup"><span data-stu-id="4226f-125">-Id</span></span>
<span data-ttu-id="4226f-126">Anger fullständigt resurs-ID för princip definitionen som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="4226f-126">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: GetByPolicyDefinitionId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4226f-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4226f-127">-InformationAction</span></span>
<span data-ttu-id="4226f-128">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="4226f-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4226f-129">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="4226f-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4226f-130">Vidare</span><span class="sxs-lookup"><span data-stu-id="4226f-130">Continue</span></span>
- <span data-ttu-id="4226f-131">Över</span><span class="sxs-lookup"><span data-stu-id="4226f-131">Ignore</span></span>
- <span data-ttu-id="4226f-132">Inquire</span><span class="sxs-lookup"><span data-stu-id="4226f-132">Inquire</span></span>
- <span data-ttu-id="4226f-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4226f-133">SilentlyContinue</span></span>
- <span data-ttu-id="4226f-134">Stanna</span><span class="sxs-lookup"><span data-stu-id="4226f-134">Stop</span></span>
- <span data-ttu-id="4226f-135">Avbryt</span><span class="sxs-lookup"><span data-stu-id="4226f-135">Suspend</span></span>

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

### <span data-ttu-id="4226f-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4226f-136">-InformationVariable</span></span>
<span data-ttu-id="4226f-137">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="4226f-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4226f-138">-Metadata</span><span class="sxs-lookup"><span data-stu-id="4226f-138">-Metadata</span></span>
<span data-ttu-id="4226f-139">Metadata för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="4226f-139">The metadata for policy definition.</span></span> <span data-ttu-id="4226f-140">Det kan antingen vara en sökväg till ett fil namn som innehåller metadata eller metadata som sträng.</span><span class="sxs-lookup"><span data-stu-id="4226f-140">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="4226f-141">-Namn</span><span class="sxs-lookup"><span data-stu-id="4226f-141">-Name</span></span>
<span data-ttu-id="4226f-142">Anger namnet på princip definitionen som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="4226f-142">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: GetByPolicyDefintionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4226f-143">-Parameter</span><span class="sxs-lookup"><span data-stu-id="4226f-143">-Parameter</span></span>
<span data-ttu-id="4226f-144">Parameter deklarationen för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="4226f-144">The parameters declaration for policy definition.</span></span> <span data-ttu-id="4226f-145">Det kan antingen vara en sökväg till ett fil namn eller en URI som innehåller parameter deklarationen eller parameter deklarationen som sträng.</span><span class="sxs-lookup"><span data-stu-id="4226f-145">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="4226f-146">-Princip</span><span class="sxs-lookup"><span data-stu-id="4226f-146">-Policy</span></span>
<span data-ttu-id="4226f-147">Anger en ny princip regel för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="4226f-147">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="4226f-148">Du kan ange sökvägen till en. JSON-fil eller en sträng som innehåller principen i JSON-format (Java Object Notation).</span><span class="sxs-lookup"><span data-stu-id="4226f-148">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="4226f-149">-För</span><span class="sxs-lookup"><span data-stu-id="4226f-149">-Pre</span></span>
<span data-ttu-id="4226f-150">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="4226f-150">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4226f-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4226f-151">CommonParameters</span></span>
<span data-ttu-id="4226f-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4226f-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4226f-153">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4226f-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4226f-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4226f-154">INPUTS</span></span>

### <span data-ttu-id="4226f-155">Ingen</span><span class="sxs-lookup"><span data-stu-id="4226f-155">None</span></span>
<span data-ttu-id="4226f-156">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="4226f-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4226f-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4226f-157">OUTPUTS</span></span>

### <span data-ttu-id="4226f-158">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="4226f-158">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="4226f-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4226f-159">NOTES</span></span>

## <span data-ttu-id="4226f-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4226f-160">RELATED LINKS</span></span>

[<span data-ttu-id="4226f-161">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4226f-161">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="4226f-162">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4226f-162">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="4226f-163">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4226f-163">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)


