---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-Azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzPolicyDefinition.md
ms.openlocfilehash: feddd9645b22c554d5e78813194ecc8837fdf3fa
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923774"
---
# <span data-ttu-id="66c48-101">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="66c48-101">Set-AzPolicyDefinition</span></span>

## <span data-ttu-id="66c48-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="66c48-102">SYNOPSIS</span></span>
<span data-ttu-id="66c48-103">Ändrar en princip definition.</span><span class="sxs-lookup"><span data-stu-id="66c48-103">Modifies a policy definition.</span></span>

## <span data-ttu-id="66c48-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="66c48-104">SYNTAX</span></span>

### <span data-ttu-id="66c48-105">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="66c48-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="66c48-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="66c48-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="66c48-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="66c48-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="66c48-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="66c48-108">IdParameterSet</span></span>
```
Set-AzPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="66c48-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="66c48-109">DESCRIPTION</span></span>
<span data-ttu-id="66c48-110">Cmdleten **set-AzPolicyDefinition** ändrar en princip definition.</span><span class="sxs-lookup"><span data-stu-id="66c48-110">The **Set-AzPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="66c48-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="66c48-111">EXAMPLES</span></span>

### <span data-ttu-id="66c48-112">Exempel 1: Uppdatera beskrivningen av en princip definition</span><span class="sxs-lookup"><span data-stu-id="66c48-112">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="66c48-113">Det första kommandot hämtar princip definitionen med namnet VMPolicyDefinition med hjälp av Get-AzPolicyDefinition cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66c48-113">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="66c48-114">Kommandot lagrar objektet i $PolicyDefinition variabel.</span><span class="sxs-lookup"><span data-stu-id="66c48-114">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="66c48-115">Det andra kommandot uppdaterar beskrivningen av princip definitionen som identifieras av egenskapen **ResourceID** för $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="66c48-115">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="66c48-116">Exempel 2: uppdatera läget för en princip definition</span><span class="sxs-lookup"><span data-stu-id="66c48-116">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="66c48-117">Det här kommandot uppdaterar princip definitionen med namnet VMPolicyDefinition med hjälp av Set-AzPolicyDefinition cmdlet för att ange egenskapen mode till "alla".</span><span class="sxs-lookup"><span data-stu-id="66c48-117">This command updates the policy definition named VMPolicyDefinition by using the Set-AzPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

## <span data-ttu-id="66c48-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="66c48-118">PARAMETERS</span></span>

### <span data-ttu-id="66c48-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="66c48-119">-ApiVersion</span></span>
<span data-ttu-id="66c48-120">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="66c48-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="66c48-121">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="66c48-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="66c48-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66c48-122">-DefaultProfile</span></span>
<span data-ttu-id="66c48-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="66c48-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66c48-124">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="66c48-124">-Description</span></span>
<span data-ttu-id="66c48-125">Anger en ny beskrivning för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="66c48-125">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="66c48-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="66c48-126">-DisplayName</span></span>
<span data-ttu-id="66c48-127">Anger ett nytt visnings namn för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="66c48-127">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="66c48-128">-ID</span><span class="sxs-lookup"><span data-stu-id="66c48-128">-Id</span></span>
<span data-ttu-id="66c48-129">Anger fullständigt resurs-ID för princip definitionen som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="66c48-129">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="66c48-130">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="66c48-130">-InformationAction</span></span>
<span data-ttu-id="66c48-131">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="66c48-131">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="66c48-132">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="66c48-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="66c48-133">Vidare</span><span class="sxs-lookup"><span data-stu-id="66c48-133">Continue</span></span>
- <span data-ttu-id="66c48-134">Över</span><span class="sxs-lookup"><span data-stu-id="66c48-134">Ignore</span></span>
- <span data-ttu-id="66c48-135">Inquire</span><span class="sxs-lookup"><span data-stu-id="66c48-135">Inquire</span></span>
- <span data-ttu-id="66c48-136">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="66c48-136">SilentlyContinue</span></span>
- <span data-ttu-id="66c48-137">Stanna</span><span class="sxs-lookup"><span data-stu-id="66c48-137">Stop</span></span>
- <span data-ttu-id="66c48-138">Avbryt</span><span class="sxs-lookup"><span data-stu-id="66c48-138">Suspend</span></span>

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

### <span data-ttu-id="66c48-139">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="66c48-139">-InformationVariable</span></span>
<span data-ttu-id="66c48-140">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="66c48-140">Specifies an information variable.</span></span>

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

### <span data-ttu-id="66c48-141">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="66c48-141">-ManagementGroupName</span></span>
<span data-ttu-id="66c48-142">Namnet på hanterings gruppen för princip definitionen som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="66c48-142">The name of the management group of the policy definition to update.</span></span>

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

### <span data-ttu-id="66c48-143">-Metadata</span><span class="sxs-lookup"><span data-stu-id="66c48-143">-Metadata</span></span>
<span data-ttu-id="66c48-144">Metadata för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="66c48-144">The metadata for policy definition.</span></span> <span data-ttu-id="66c48-145">Det kan antingen vara en sökväg till ett fil namn som innehåller metadata eller metadata som sträng.</span><span class="sxs-lookup"><span data-stu-id="66c48-145">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="66c48-146">-Mode</span><span class="sxs-lookup"><span data-stu-id="66c48-146">-Mode</span></span>
<span data-ttu-id="66c48-147">Läget för den nya princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="66c48-147">The mode of the new policy definition.</span></span>

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

### <span data-ttu-id="66c48-148">-Namn</span><span class="sxs-lookup"><span data-stu-id="66c48-148">-Name</span></span>
<span data-ttu-id="66c48-149">Anger namnet på princip definitionen som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="66c48-149">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="66c48-150">-Parameter</span><span class="sxs-lookup"><span data-stu-id="66c48-150">-Parameter</span></span>
<span data-ttu-id="66c48-151">Parameter deklarationen för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="66c48-151">The parameters declaration for policy definition.</span></span> <span data-ttu-id="66c48-152">Det kan antingen vara en sökväg till ett fil namn eller en URI som innehåller parameter deklarationen eller parameter deklarationen som sträng.</span><span class="sxs-lookup"><span data-stu-id="66c48-152">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="66c48-153">-Princip</span><span class="sxs-lookup"><span data-stu-id="66c48-153">-Policy</span></span>
<span data-ttu-id="66c48-154">Anger en ny princip regel för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="66c48-154">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="66c48-155">Du kan ange sökvägen till en. JSON-fil eller en sträng som innehåller principen i JSON-format (Java Object Notation).</span><span class="sxs-lookup"><span data-stu-id="66c48-155">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="66c48-156">-För</span><span class="sxs-lookup"><span data-stu-id="66c48-156">-Pre</span></span>
<span data-ttu-id="66c48-157">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="66c48-157">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="66c48-158">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="66c48-158">-SubscriptionId</span></span>
<span data-ttu-id="66c48-159">Abonnemangs-ID för princip definitionen som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="66c48-159">The subscription ID of the policy definition to update.</span></span>

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

### <span data-ttu-id="66c48-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66c48-160">CommonParameters</span></span>
<span data-ttu-id="66c48-161">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66c48-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66c48-162">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66c48-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66c48-163">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="66c48-163">INPUTS</span></span>

## <span data-ttu-id="66c48-164">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="66c48-164">OUTPUTS</span></span>

## <span data-ttu-id="66c48-165">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="66c48-165">NOTES</span></span>

## <span data-ttu-id="66c48-166">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="66c48-166">RELATED LINKS</span></span>

[<span data-ttu-id="66c48-167">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="66c48-167">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="66c48-168">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="66c48-168">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="66c48-169">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="66c48-169">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)


