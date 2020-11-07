---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplication.md
ms.openlocfilehash: 75e750aa13df16deb5c281a5914a6c21a1740e88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757474"
---
# <span data-ttu-id="4c06c-101">Remove-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="4c06c-101">Remove-AzureRmManagedApplication</span></span>

## <span data-ttu-id="4c06c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4c06c-102">SYNOPSIS</span></span>
<span data-ttu-id="4c06c-103">Tar bort ett hanterat program</span><span class="sxs-lookup"><span data-stu-id="4c06c-103">Removes a managed application</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c06c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4c06c-104">SYNTAX</span></span>

### <span data-ttu-id="4c06c-105">Parametern för hanterade program namn.</span><span class="sxs-lookup"><span data-stu-id="4c06c-105">The managed application name parameter set.</span></span> <span data-ttu-id="4c06c-106">Vis</span><span class="sxs-lookup"><span data-stu-id="4c06c-106">(Default)</span></span>
```
Remove-AzureRmManagedApplication -Name <String> -ResourceGroupName <String> [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c06c-107">Parametern hanterad program-ID.</span><span class="sxs-lookup"><span data-stu-id="4c06c-107">The managed application Id parameter set.</span></span>
```
Remove-AzureRmManagedApplication -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c06c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4c06c-108">DESCRIPTION</span></span>
<span data-ttu-id="4c06c-109">Cmdleten **Remove-AzureRmManagedApplication** tar bort ett hanterat program</span><span class="sxs-lookup"><span data-stu-id="4c06c-109">The **Remove-AzureRmManagedApplication** cmdlet removes a managed application</span></span>

## <span data-ttu-id="4c06c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4c06c-110">EXAMPLES</span></span>

### <span data-ttu-id="4c06c-111">Exempel 1: ta bort hanterat program via resurs-ID</span><span class="sxs-lookup"><span data-stu-id="4c06c-111">Example 1: Remove managed application by resource ID</span></span>
```
PS C:\>$Application = Get-AzureRmManagedApplication -Name "myApp" -ResourceGroupName "myRG"
PS C:\>Remove-AzureRmManagedApplication -Id $Application.ResourceId -Force
```

<span data-ttu-id="4c06c-112">Det första kommandot får ett hanterat program som heter Mittprog med hjälp av Get-AzureRmManagedApplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c06c-112">The first command gets a managed application named myApp by using the Get-AzureRmManagedApplication cmdlet.</span></span>
<span data-ttu-id="4c06c-113">Kommandot sparar det i $Application variabel.</span><span class="sxs-lookup"><span data-stu-id="4c06c-113">The command stores it in the $Application variable.</span></span>

<span data-ttu-id="4c06c-114">Det andra kommandot tar bort det hanterade programmet som identifieras av egenskapen **ResourceID** för $application.</span><span class="sxs-lookup"><span data-stu-id="4c06c-114">The second command removes the managed application identified by the **ResourceId** property of $Application.</span></span>

## <span data-ttu-id="4c06c-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4c06c-115">PARAMETERS</span></span>

### <span data-ttu-id="4c06c-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4c06c-116">-ApiVersion</span></span>
<span data-ttu-id="4c06c-117">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="4c06c-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="4c06c-118">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="4c06c-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="4c06c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c06c-119">-DefaultProfile</span></span>
<span data-ttu-id="4c06c-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4c06c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c06c-121">-Force</span><span class="sxs-lookup"><span data-stu-id="4c06c-121">-Force</span></span>
<span data-ttu-id="4c06c-122">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="4c06c-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4c06c-123">-ID</span><span class="sxs-lookup"><span data-stu-id="4c06c-123">-Id</span></span>
<span data-ttu-id="4c06c-124">Fullständigt kvalificerat program-ID, inklusive prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="4c06c-124">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="4c06c-125">till exempel/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="4c06c-125">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c06c-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="4c06c-126">-Name</span></span>
<span data-ttu-id="4c06c-127">Namnet på det hanterade programmet.</span><span class="sxs-lookup"><span data-stu-id="4c06c-127">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c06c-128">-För</span><span class="sxs-lookup"><span data-stu-id="4c06c-128">-Pre</span></span>
<span data-ttu-id="4c06c-129">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="4c06c-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="4c06c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c06c-130">-ResourceGroupName</span></span>
<span data-ttu-id="4c06c-131">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="4c06c-131">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c06c-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4c06c-132">-Confirm</span></span>
<span data-ttu-id="4c06c-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4c06c-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c06c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c06c-134">-WhatIf</span></span>
<span data-ttu-id="4c06c-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4c06c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c06c-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4c06c-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c06c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c06c-137">CommonParameters</span></span>
<span data-ttu-id="4c06c-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c06c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c06c-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c06c-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c06c-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4c06c-140">INPUTS</span></span>

### <span data-ttu-id="4c06c-141">System. String</span><span class="sxs-lookup"><span data-stu-id="4c06c-141">System.String</span></span>

## <span data-ttu-id="4c06c-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4c06c-142">OUTPUTS</span></span>

### <span data-ttu-id="4c06c-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4c06c-143">System.Boolean</span></span>

## <span data-ttu-id="4c06c-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4c06c-144">NOTES</span></span>

## <span data-ttu-id="4c06c-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4c06c-145">RELATED LINKS</span></span>

