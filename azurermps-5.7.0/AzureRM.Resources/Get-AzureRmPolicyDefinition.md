---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
ms.openlocfilehash: d9d79374e426c6d895fbfcef957da20ed9721f70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582003"
---
# <span data-ttu-id="9c3b4-101">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="9c3b4-101">Get-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="9c3b4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9c3b4-102">SYNOPSIS</span></span>
<span data-ttu-id="9c3b4-103">Hämtar princip definitioner.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-103">Gets policy definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c3b4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9c3b4-104">SYNTAX</span></span>

### <span data-ttu-id="9c3b4-105">GetAllPolicyDefinitions (standard)</span><span class="sxs-lookup"><span data-stu-id="9c3b4-105">GetAllPolicyDefinitions (Default)</span></span>
```
Get-AzureRmPolicyDefinition [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="9c3b4-106">GetByPolicyDefintionName</span><span class="sxs-lookup"><span data-stu-id="9c3b4-106">GetByPolicyDefintionName</span></span>
```
Get-AzureRmPolicyDefinition -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="9c3b4-107">GetByPolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="9c3b4-107">GetByPolicyDefinitionId</span></span>
```
Get-AzureRmPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="9c3b4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9c3b4-108">DESCRIPTION</span></span>
<span data-ttu-id="9c3b4-109">Cmdleten **Get-AzureRmPolicyDefinition** hämtar alla princip definitioner eller en specifik princip definition som identifieras med namn eller ID.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-109">The **Get-AzureRmPolicyDefinition** cmdlet gets all the policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="9c3b4-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9c3b4-110">EXAMPLES</span></span>

### <span data-ttu-id="9c3b4-111">Exempel 1: Hämta alla princip definitioner</span><span class="sxs-lookup"><span data-stu-id="9c3b4-111">Example 1: Get all policy definition</span></span>
```
PS C:\>Get-AzureRmPolicyDefinition
```

<span data-ttu-id="9c3b4-112">Det här kommandot får alla princip definitioner.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-112">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="9c3b4-113">Exempel 2: Hämta princip definition efter namn</span><span class="sxs-lookup"><span data-stu-id="9c3b4-113">Example 2: Get policy definition by name</span></span>
```
PS C:\>Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="9c3b4-114">Det här kommandot får princip definitionen med namnet VMPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-114">This command gets the policy definition named VMPolicyDefinition.</span></span>

## <span data-ttu-id="9c3b4-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9c3b4-115">PARAMETERS</span></span>

### <span data-ttu-id="9c3b4-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9c3b4-116">-ApiVersion</span></span>
<span data-ttu-id="9c3b4-117">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-117">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="9c3b4-118">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="9c3b4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c3b4-119">-DefaultProfile</span></span>
<span data-ttu-id="9c3b4-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="9c3b4-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9c3b4-121">-ID</span><span class="sxs-lookup"><span data-stu-id="9c3b4-121">-Id</span></span>
<span data-ttu-id="9c3b4-122">Anger det fullständigt kvalificerade resurs-ID för princip definitionen som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-122">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9c3b4-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="9c3b4-123">-InformationAction</span></span>
<span data-ttu-id="9c3b4-124">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9c3b4-125">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="9c3b4-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9c3b4-126">Vidare</span><span class="sxs-lookup"><span data-stu-id="9c3b4-126">Continue</span></span>
- <span data-ttu-id="9c3b4-127">Över</span><span class="sxs-lookup"><span data-stu-id="9c3b4-127">Ignore</span></span>
- <span data-ttu-id="9c3b4-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="9c3b4-128">Inquire</span></span>
- <span data-ttu-id="9c3b4-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9c3b4-129">SilentlyContinue</span></span>
- <span data-ttu-id="9c3b4-130">Stanna</span><span class="sxs-lookup"><span data-stu-id="9c3b4-130">Stop</span></span>
- <span data-ttu-id="9c3b4-131">Avbryt</span><span class="sxs-lookup"><span data-stu-id="9c3b4-131">Suspend</span></span>

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

### <span data-ttu-id="9c3b4-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9c3b4-132">-InformationVariable</span></span>
<span data-ttu-id="9c3b4-133">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9c3b4-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="9c3b4-134">-Name</span></span>
<span data-ttu-id="9c3b4-135">Anger namnet på den princip definition som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-135">Specifies the name of the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9c3b4-136">-För</span><span class="sxs-lookup"><span data-stu-id="9c3b4-136">-Pre</span></span>
<span data-ttu-id="9c3b4-137">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="9c3b4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c3b4-138">CommonParameters</span></span>
<span data-ttu-id="9c3b4-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c3b4-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c3b4-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c3b4-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9c3b4-141">INPUTS</span></span>

### <span data-ttu-id="9c3b4-142">Ingen</span><span class="sxs-lookup"><span data-stu-id="9c3b4-142">None</span></span>
<span data-ttu-id="9c3b4-143">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="9c3b4-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9c3b4-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9c3b4-144">OUTPUTS</span></span>

### <span data-ttu-id="9c3b4-145">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="9c3b4-145">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="9c3b4-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9c3b4-146">NOTES</span></span>

## <span data-ttu-id="9c3b4-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9c3b4-147">RELATED LINKS</span></span>

[<span data-ttu-id="9c3b4-148">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="9c3b4-148">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="9c3b4-149">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="9c3b4-149">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="9c3b4-150">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="9c3b4-150">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


