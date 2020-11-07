---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyDefinition.md
ms.openlocfilehash: 2404c0f2dc6c357503f23e7ed509f1c58c352c8a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757466"
---
# <span data-ttu-id="a8126-101">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a8126-101">Set-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="a8126-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a8126-102">SYNOPSIS</span></span>
<span data-ttu-id="a8126-103">Ändrar en princip definition.</span><span class="sxs-lookup"><span data-stu-id="a8126-103">Modifies a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8126-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a8126-104">SYNTAX</span></span>

### <span data-ttu-id="a8126-105">Parametern för princip definitions namn.</span><span class="sxs-lookup"><span data-stu-id="a8126-105">The policy definition name parameter set.</span></span> <span data-ttu-id="a8126-106">Vis</span><span class="sxs-lookup"><span data-stu-id="a8126-106">(Default)</span></span>
```
Set-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a8126-107">Parameter uppsättning för princip Definitions-ID.</span><span class="sxs-lookup"><span data-stu-id="a8126-107">The policy definition Id parameter set.</span></span>
```
Set-AzureRmPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a8126-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a8126-108">DESCRIPTION</span></span>
<span data-ttu-id="a8126-109">Cmdleten **set-AzureRmPolicyDefinition** ändrar en princip definition.</span><span class="sxs-lookup"><span data-stu-id="a8126-109">The **Set-AzureRmPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="a8126-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a8126-110">EXAMPLES</span></span>

### <span data-ttu-id="a8126-111">Exempel 1: Uppdatera beskrivningen av en princip definition</span><span class="sxs-lookup"><span data-stu-id="a8126-111">Example 1: Update the description of a policy definition</span></span>
```
PS C:\>$PolicyDefinition = Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
PS C:\> Set-AzureRmPolicyDefinition -Id $Policy.ResourceId -Description "Updated policy to not allow virtual machine creation"
```

<span data-ttu-id="a8126-112">Det första kommandot hämtar princip definitionen med namnet VMPolicyDefinition med hjälp av Get-AzureRmPolicyDefinition cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8126-112">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="a8126-113">Kommandot lagrar objektet i $PolicyDefinition variabel.</span><span class="sxs-lookup"><span data-stu-id="a8126-113">The command stores that object in the $PolicyDefinition variable.</span></span>

<span data-ttu-id="a8126-114">Det andra kommandot uppdaterar beskrivningen av princip definitionen som identifieras av egenskapen **ResourceID** för $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="a8126-114">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="a8126-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a8126-115">PARAMETERS</span></span>

### <span data-ttu-id="a8126-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a8126-116">-ApiVersion</span></span>
<span data-ttu-id="a8126-117">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="a8126-117">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="a8126-118">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="a8126-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="a8126-119">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="a8126-119">-Description</span></span>
<span data-ttu-id="a8126-120">Anger en ny beskrivning för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="a8126-120">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="a8126-121">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a8126-121">-DisplayName</span></span>
<span data-ttu-id="a8126-122">Anger ett nytt visnings namn för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="a8126-122">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="a8126-123">-ID</span><span class="sxs-lookup"><span data-stu-id="a8126-123">-Id</span></span>
<span data-ttu-id="a8126-124">Anger fullständigt resurs-ID för princip definitionen som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="a8126-124">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8126-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a8126-125">-InformationAction</span></span>
<span data-ttu-id="a8126-126">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="a8126-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a8126-127">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a8126-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a8126-128">Vidare</span><span class="sxs-lookup"><span data-stu-id="a8126-128">Continue</span></span>
- <span data-ttu-id="a8126-129">Över</span><span class="sxs-lookup"><span data-stu-id="a8126-129">Ignore</span></span>
- <span data-ttu-id="a8126-130">Inquire</span><span class="sxs-lookup"><span data-stu-id="a8126-130">Inquire</span></span>
- <span data-ttu-id="a8126-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a8126-131">SilentlyContinue</span></span>
- <span data-ttu-id="a8126-132">Stanna</span><span class="sxs-lookup"><span data-stu-id="a8126-132">Stop</span></span>
- <span data-ttu-id="a8126-133">Avbryt</span><span class="sxs-lookup"><span data-stu-id="a8126-133">Suspend</span></span>

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

### <span data-ttu-id="a8126-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a8126-134">-InformationVariable</span></span>
<span data-ttu-id="a8126-135">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="a8126-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a8126-136">-Namn</span><span class="sxs-lookup"><span data-stu-id="a8126-136">-Name</span></span>
<span data-ttu-id="a8126-137">Anger namnet på princip definitionen som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="a8126-137">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8126-138">-Princip</span><span class="sxs-lookup"><span data-stu-id="a8126-138">-Policy</span></span>
<span data-ttu-id="a8126-139">Anger en ny princip regel för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="a8126-139">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="a8126-140">Du kan ange sökvägen till en. JSON-fil eller en sträng som innehåller principen i JSON-format (Java Object Notation).</span><span class="sxs-lookup"><span data-stu-id="a8126-140">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="a8126-141">-För</span><span class="sxs-lookup"><span data-stu-id="a8126-141">-Pre</span></span>
<span data-ttu-id="a8126-142">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="a8126-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a8126-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8126-143">-DefaultProfile</span></span>
<span data-ttu-id="a8126-144">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a8126-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8126-145">-Metadata</span><span class="sxs-lookup"><span data-stu-id="a8126-145">-Metadata</span></span>
<span data-ttu-id="a8126-146">Metadata för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="a8126-146">The metadata for policy definition.</span></span> <span data-ttu-id="a8126-147">Det kan antingen vara en sökväg till ett fil namn som innehåller metadata eller metadata som sträng.</span><span class="sxs-lookup"><span data-stu-id="a8126-147">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="a8126-148">-Parameter</span><span class="sxs-lookup"><span data-stu-id="a8126-148">-Parameter</span></span>
<span data-ttu-id="a8126-149">Parameter deklarationen för princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="a8126-149">The parameters declaration for policy definition.</span></span> <span data-ttu-id="a8126-150">Det kan antingen vara en sökväg till ett fil namn eller en URI som innehåller parameter deklarationen eller parameter deklarationen som sträng.</span><span class="sxs-lookup"><span data-stu-id="a8126-150">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="a8126-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8126-151">CommonParameters</span></span>
<span data-ttu-id="a8126-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8126-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8126-153">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8126-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8126-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a8126-154">INPUTS</span></span>

## <span data-ttu-id="a8126-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a8126-155">OUTPUTS</span></span>

### <span data-ttu-id="a8126-156">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="a8126-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a8126-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a8126-157">NOTES</span></span>

## <span data-ttu-id="a8126-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a8126-158">RELATED LINKS</span></span>

[<span data-ttu-id="a8126-159">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a8126-159">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="a8126-160">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a8126-160">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="a8126-161">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a8126-161">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)


