---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyDefinition.md
ms.openlocfilehash: 4f71814790d5c543a867ad4de0aaac37c98079a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583983"
---
# <span data-ttu-id="a941e-101">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a941e-101">Set-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="a941e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a941e-102">SYNOPSIS</span></span>
<span data-ttu-id="a941e-103">Ändrar en princip definition.</span><span class="sxs-lookup"><span data-stu-id="a941e-103">Modifies a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a941e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a941e-104">SYNTAX</span></span>

### <span data-ttu-id="a941e-105">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a941e-105">NameParameterSet (Default)</span></span>
```
Set-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a941e-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a941e-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a941e-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a941e-107">SubscriptionIdParameterSet</span></span>
```
Set-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a941e-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a941e-108">IdParameterSet</span></span>
```
Set-AzureRmPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a941e-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a941e-109">DESCRIPTION</span></span>
<span data-ttu-id="a941e-110">Cmdleten **set-AzureRmPolicyDefinition** ändrar en princip definition.</span><span class="sxs-lookup"><span data-stu-id="a941e-110">The **Set-AzureRmPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="a941e-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a941e-111">EXAMPLES</span></span>

### <span data-ttu-id="a941e-112">Exempel 1: Uppdatera beskrivningen av en princip definition</span><span class="sxs-lookup"><span data-stu-id="a941e-112">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzureRmPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzureRmPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="a941e-113">Det första kommandot hämtar princip definitionen med namnet VMPolicyDefinition med hjälp av Get-AzureRmPolicyDefinition cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a941e-113">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="a941e-114">Kommandot lagrar objektet i $PolicyDefinition variabel.</span><span class="sxs-lookup"><span data-stu-id="a941e-114">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="a941e-115">Det andra kommandot uppdaterar beskrivningen av princip definitionen som identifieras av egenskapen **ResourceID** för $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="a941e-115">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="a941e-116">Exempel 2: uppdatera läget för en princip definition</span><span class="sxs-lookup"><span data-stu-id="a941e-116">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzureRmPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="a941e-117">Det här kommandot uppdaterar princip definitionen med namnet VMPolicyDefinition med hjälp av Set-AzureRmPolicyDefinition cmdlet för att ange egenskapen mode till "alla".</span><span class="sxs-lookup"><span data-stu-id="a941e-117">This command updates the policy definition named VMPolicyDefinition by using the Set-AzureRmPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

## <span data-ttu-id="a941e-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a941e-118">PARAMETERS</span></span>

### <span data-ttu-id="a941e-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a941e-119">-ApiVersion</span></span>
<span data-ttu-id="a941e-120">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="a941e-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="a941e-121">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="a941e-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="a941e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a941e-122">-DefaultProfile</span></span>
<span data-ttu-id="a941e-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a941e-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a941e-124">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="a941e-124">-Description</span></span>
<span data-ttu-id="a941e-125">Anger en ny beskrivning för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="a941e-125">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="a941e-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a941e-126">-DisplayName</span></span>
<span data-ttu-id="a941e-127">Anger ett nytt visnings namn för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="a941e-127">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="a941e-128">-ID</span><span class="sxs-lookup"><span data-stu-id="a941e-128">-Id</span></span>
<span data-ttu-id="a941e-129">Anger fullständigt resurs-ID för princip definitionen som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="a941e-129">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a941e-130">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a941e-130">-InformationAction</span></span>
<span data-ttu-id="a941e-131">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="a941e-131">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="a941e-132">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a941e-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a941e-133">Vidare</span><span class="sxs-lookup"><span data-stu-id="a941e-133">Continue</span></span>
- <span data-ttu-id="a941e-134">Över</span><span class="sxs-lookup"><span data-stu-id="a941e-134">Ignore</span></span>
- <span data-ttu-id="a941e-135">Inquire</span><span class="sxs-lookup"><span data-stu-id="a941e-135">Inquire</span></span>
- <span data-ttu-id="a941e-136">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a941e-136">SilentlyContinue</span></span>
- <span data-ttu-id="a941e-137">Stanna</span><span class="sxs-lookup"><span data-stu-id="a941e-137">Stop</span></span>
- <span data-ttu-id="a941e-138">Avbryt</span><span class="sxs-lookup"><span data-stu-id="a941e-138">Suspend</span></span>

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

### <span data-ttu-id="a941e-139">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a941e-139">-InformationVariable</span></span>
<span data-ttu-id="a941e-140">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="a941e-140">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a941e-141">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="a941e-141">-ManagementGroupName</span></span>
<span data-ttu-id="a941e-142">Namnet på hanterings gruppen för princip definitionen som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="a941e-142">The name of the management group of the policy definition to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a941e-143">-Metadata</span><span class="sxs-lookup"><span data-stu-id="a941e-143">-Metadata</span></span>
<span data-ttu-id="a941e-144">Metadata för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="a941e-144">The metadata for policy definition.</span></span> <span data-ttu-id="a941e-145">Det kan antingen vara en sökväg till ett fil namn som innehåller metadata eller metadata som sträng.</span><span class="sxs-lookup"><span data-stu-id="a941e-145">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="a941e-146">-Mode</span><span class="sxs-lookup"><span data-stu-id="a941e-146">-Mode</span></span>
<span data-ttu-id="a941e-147">Läget för den nya princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="a941e-147">The mode of the new policy definition.</span></span>

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

### <span data-ttu-id="a941e-148">-Namn</span><span class="sxs-lookup"><span data-stu-id="a941e-148">-Name</span></span>
<span data-ttu-id="a941e-149">Anger namnet på princip definitionen som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="a941e-149">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a941e-150">-Parameter</span><span class="sxs-lookup"><span data-stu-id="a941e-150">-Parameter</span></span>
<span data-ttu-id="a941e-151">Parameter deklarationen för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="a941e-151">The parameters declaration for policy definition.</span></span> <span data-ttu-id="a941e-152">Det kan antingen vara en sökväg till ett fil namn eller en URI som innehåller parameter deklarationen eller parameter deklarationen som sträng.</span><span class="sxs-lookup"><span data-stu-id="a941e-152">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="a941e-153">-Princip</span><span class="sxs-lookup"><span data-stu-id="a941e-153">-Policy</span></span>
<span data-ttu-id="a941e-154">Anger en ny princip regel för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="a941e-154">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="a941e-155">Du kan ange sökvägen till en. JSON-fil eller en sträng som innehåller principen i JSON-format (Java Object Notation).</span><span class="sxs-lookup"><span data-stu-id="a941e-155">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="a941e-156">-För</span><span class="sxs-lookup"><span data-stu-id="a941e-156">-Pre</span></span>
<span data-ttu-id="a941e-157">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="a941e-157">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a941e-158">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a941e-158">-SubscriptionId</span></span>
<span data-ttu-id="a941e-159">Abonnemangs-ID för princip definitionen som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="a941e-159">The subscription ID of the policy definition to update.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a941e-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a941e-160">CommonParameters</span></span>
<span data-ttu-id="a941e-161">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a941e-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a941e-162">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a941e-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a941e-163">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a941e-163">INPUTS</span></span>

## <span data-ttu-id="a941e-164">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a941e-164">OUTPUTS</span></span>

## <span data-ttu-id="a941e-165">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a941e-165">NOTES</span></span>

## <span data-ttu-id="a941e-166">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a941e-166">RELATED LINKS</span></span>

[<span data-ttu-id="a941e-167">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a941e-167">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="a941e-168">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a941e-168">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="a941e-169">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a941e-169">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)


