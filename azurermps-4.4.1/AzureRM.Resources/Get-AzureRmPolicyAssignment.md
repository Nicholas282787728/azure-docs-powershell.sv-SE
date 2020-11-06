---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
ms.openlocfilehash: 11a28cb8848c197d9d766b05833e8c0ca3106412
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575857"
---
# <span data-ttu-id="2fcb8-101">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="2fcb8-101">Get-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="2fcb8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2fcb8-102">SYNOPSIS</span></span>
<span data-ttu-id="2fcb8-103">Hämtar princip tilldelningar.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-103">Gets policy assignments.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fcb8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2fcb8-104">SYNTAX</span></span>

### <span data-ttu-id="2fcb8-105">Parametern lista alla princip tilldelningar.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-105">The list all policy assignments parameter set.</span></span> <span data-ttu-id="2fcb8-106">Vis</span><span class="sxs-lookup"><span data-stu-id="2fcb8-106">(Default)</span></span>
```
Get-AzureRmPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="2fcb8-107">Parametern för princip tilldelnings namn.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-107">The policy assignment name parameter set.</span></span>
```
Get-AzureRmPolicyAssignment [-Name <String>] -Scope <String> [-PolicyDefinitionId <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="2fcb8-108">ID-parametern för princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-108">The policy assignment Id parameter set.</span></span>
```
Get-AzureRmPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2fcb8-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2fcb8-109">DESCRIPTION</span></span>
<span data-ttu-id="2fcb8-110">Cmdleten **Get-AzureRmPolicyAssignment** hämtar alla princip tilldelningar eller särskilda uppgifter.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-110">The **Get-AzureRmPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="2fcb8-111">Identifiera en princip tilldelning för att få namn och räckvidd eller efter ID.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-111">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="2fcb8-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2fcb8-112">EXAMPLES</span></span>

### <span data-ttu-id="2fcb8-113">Exempel 1: Hämta alla princip tilldelningar</span><span class="sxs-lookup"><span data-stu-id="2fcb8-113">Example 1: Get all policy assignments</span></span>
```
PS C:\>Get-AzureRmPolicyAssignment
```

<span data-ttu-id="2fcb8-114">Det här kommandot får alla princip tilldelningar.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-114">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="2fcb8-115">Exempel 2: Hämta en specifik princip tilldelning</span><span class="sxs-lookup"><span data-stu-id="2fcb8-115">Example 2: Get a specific policy assignment</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> Get-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="2fcb8-116">Det första kommandot får en resurs grupp som heter ResourceGroup11 med hjälp av Get-AzureRMResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="2fcb8-117">Kommandot lagrar objektet i $ResourceGroup variabel.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-117">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="2fcb8-118">Det andra kommandot Hämta princip tilldelningen med namnet PolicyAssignment07 för omfattningen som egenskapen **ResourceID** för $ResourceGroup identifierar.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-118">The second command get the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

## <span data-ttu-id="2fcb8-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2fcb8-119">PARAMETERS</span></span>

### <span data-ttu-id="2fcb8-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2fcb8-120">-ApiVersion</span></span>
<span data-ttu-id="2fcb8-121">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="2fcb8-122">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-122">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="2fcb8-123">-ID</span><span class="sxs-lookup"><span data-stu-id="2fcb8-123">-Id</span></span>
<span data-ttu-id="2fcb8-124">Anger det fullständigt kvalificerade resurs-ID för princip tilldelningen som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-124">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fcb8-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2fcb8-125">-InformationAction</span></span>
<span data-ttu-id="2fcb8-126">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2fcb8-127">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="2fcb8-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2fcb8-128">Vidare</span><span class="sxs-lookup"><span data-stu-id="2fcb8-128">Continue</span></span>
- <span data-ttu-id="2fcb8-129">Över</span><span class="sxs-lookup"><span data-stu-id="2fcb8-129">Ignore</span></span>
- <span data-ttu-id="2fcb8-130">Inquire</span><span class="sxs-lookup"><span data-stu-id="2fcb8-130">Inquire</span></span>
- <span data-ttu-id="2fcb8-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2fcb8-131">SilentlyContinue</span></span>
- <span data-ttu-id="2fcb8-132">Stanna</span><span class="sxs-lookup"><span data-stu-id="2fcb8-132">Stop</span></span>
- <span data-ttu-id="2fcb8-133">Avbryt</span><span class="sxs-lookup"><span data-stu-id="2fcb8-133">Suspend</span></span>

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

### <span data-ttu-id="2fcb8-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2fcb8-134">-InformationVariable</span></span>
<span data-ttu-id="2fcb8-135">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2fcb8-136">-Namn</span><span class="sxs-lookup"><span data-stu-id="2fcb8-136">-Name</span></span>
<span data-ttu-id="2fcb8-137">Anger namnet på den princip tilldelning som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-137">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fcb8-138">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="2fcb8-138">-PolicyDefinitionId</span></span>
<span data-ttu-id="2fcb8-139">Anger ID för princip definitionen för de princip tilldelningar som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-139">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set., The policy assignment Id parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fcb8-140">-För</span><span class="sxs-lookup"><span data-stu-id="2fcb8-140">-Pre</span></span>
<span data-ttu-id="2fcb8-141">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="2fcb8-142">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="2fcb8-142">-Scope</span></span>
<span data-ttu-id="2fcb8-143">Anger det område där principen tillämpas för den uppgift som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-143">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fcb8-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fcb8-144">-DefaultProfile</span></span>
<span data-ttu-id="2fcb8-145">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2fcb8-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fcb8-146">CommonParameters</span></span>
<span data-ttu-id="2fcb8-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fcb8-148">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fcb8-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fcb8-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2fcb8-149">INPUTS</span></span>

## <span data-ttu-id="2fcb8-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2fcb8-150">OUTPUTS</span></span>

### <span data-ttu-id="2fcb8-151">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="2fcb8-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="2fcb8-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2fcb8-152">NOTES</span></span>

## <span data-ttu-id="2fcb8-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2fcb8-153">RELATED LINKS</span></span>

[<span data-ttu-id="2fcb8-154">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="2fcb8-154">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="2fcb8-155">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="2fcb8-155">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="2fcb8-156">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="2fcb8-156">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


