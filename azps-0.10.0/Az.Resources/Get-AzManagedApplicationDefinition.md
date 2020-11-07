---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzManagedApplicationDefinition.md
ms.openlocfilehash: 4623634d72e78ab62deca43da698d218ddb9276e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924022"
---
# <span data-ttu-id="511e2-101">Get-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="511e2-101">Get-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="511e2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="511e2-102">SYNOPSIS</span></span>
<span data-ttu-id="511e2-103">Hämtar definitioner för hanterade program</span><span class="sxs-lookup"><span data-stu-id="511e2-103">Gets managed application definitions</span></span>

## <span data-ttu-id="511e2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="511e2-104">SYNTAX</span></span>

### <span data-ttu-id="511e2-105">GetByNameAndResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="511e2-105">GetByNameAndResourceGroup (Default)</span></span>
```
Get-AzManagedApplicationDefinition [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="511e2-106">GetById</span><span class="sxs-lookup"><span data-stu-id="511e2-106">GetById</span></span>
```
Get-AzManagedApplicationDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="511e2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="511e2-107">DESCRIPTION</span></span>
<span data-ttu-id="511e2-108">Cmdleten **Get-AzManagedApplicationDefinition** hämtar definitioner för hanterade program</span><span class="sxs-lookup"><span data-stu-id="511e2-108">The **Get-AzManagedApplicationDefinition** cmdlet gets managed application definitions</span></span>

## <span data-ttu-id="511e2-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="511e2-109">EXAMPLES</span></span>

### <span data-ttu-id="511e2-110">Exempel 1: Hämta alla definitioner för hanterade program under en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="511e2-110">Example 1: Get all managed application definitions under a resource group</span></span>
```
PS C:\>Get-AzManagedApplicationDefinition -ResourceGroupName "MyRG"
```

<span data-ttu-id="511e2-111">Det här kommandot hämtar definitionerna för hanterade program under resurs gruppen "MyRG"</span><span class="sxs-lookup"><span data-stu-id="511e2-111">This command gets the managed application definitions under resource group "MyRG"</span></span>

### <span data-ttu-id="511e2-112">Exempel 2: Hämta ett hanterat program</span><span class="sxs-lookup"><span data-stu-id="511e2-112">Example 2: Get a managed application definition</span></span>
```
PS C:\>Get-AzManagedApplicationDefinition -ResourceGroupName "MyRG" -Name "myManagedAppDef"
```

<span data-ttu-id="511e2-113">Det här kommandot får den hanterade program definitionen "myManagedAppDef" under resurs gruppen "MyRG"</span><span class="sxs-lookup"><span data-stu-id="511e2-113">This command gets the managed application definition "myManagedAppDef" under resource group "MyRG"</span></span>

## <span data-ttu-id="511e2-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="511e2-114">PARAMETERS</span></span>

### <span data-ttu-id="511e2-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="511e2-115">-ApiVersion</span></span>
<span data-ttu-id="511e2-116">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="511e2-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="511e2-117">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="511e2-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="511e2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="511e2-118">-DefaultProfile</span></span>
<span data-ttu-id="511e2-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="511e2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="511e2-120">-ID</span><span class="sxs-lookup"><span data-stu-id="511e2-120">-Id</span></span>
<span data-ttu-id="511e2-121">Fullständigt kvalificerat ID för hanterade program, inklusive prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="511e2-121">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="511e2-122">till exempel/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="511e2-122">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases: ResourceId, ManagedApplicationDefinitionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="511e2-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="511e2-123">-Name</span></span>
<span data-ttu-id="511e2-124">Det hanterade programmets definitions namn.</span><span class="sxs-lookup"><span data-stu-id="511e2-124">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="511e2-125">-För</span><span class="sxs-lookup"><span data-stu-id="511e2-125">-Pre</span></span>
<span data-ttu-id="511e2-126">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="511e2-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="511e2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="511e2-127">-ResourceGroupName</span></span>
<span data-ttu-id="511e2-128">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="511e2-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="511e2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="511e2-129">CommonParameters</span></span>
<span data-ttu-id="511e2-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="511e2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="511e2-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="511e2-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="511e2-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="511e2-132">INPUTS</span></span>

### <span data-ttu-id="511e2-133">System. String</span><span class="sxs-lookup"><span data-stu-id="511e2-133">System.String</span></span>

## <span data-ttu-id="511e2-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="511e2-134">OUTPUTS</span></span>

### <span data-ttu-id="511e2-135">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="511e2-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="511e2-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="511e2-136">NOTES</span></span>

## <span data-ttu-id="511e2-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="511e2-137">RELATED LINKS</span></span>
