---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzIotSecuritySolution.md
ms.openlocfilehash: 42e483a9783a919dfe45425357052df2389cc8b0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261701"
---
# <span data-ttu-id="7298d-101">Remove-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="7298d-101">Remove-AzIotSecuritySolution</span></span>

## <span data-ttu-id="7298d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7298d-102">SYNOPSIS</span></span>
<span data-ttu-id="7298d-103">Ta bort IoT-säkerhetslösning</span><span class="sxs-lookup"><span data-stu-id="7298d-103">Delete IoT security solution</span></span>

## <span data-ttu-id="7298d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7298d-104">SYNTAX</span></span>

### <span data-ttu-id="7298d-105">ResourceGroupLevelResource (standard)</span><span class="sxs-lookup"><span data-stu-id="7298d-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7298d-106">ID</span><span class="sxs-lookup"><span data-stu-id="7298d-106">ResourceId</span></span>
```
Remove-AzIotSecuritySolution -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7298d-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="7298d-107">InputObject</span></span>
```
Remove-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7298d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7298d-108">DESCRIPTION</span></span>
<span data-ttu-id="7298d-109">Remove-AzIotSecuritySolution cmdlet tar bort en specifik IoT-säkerhetslösning.</span><span class="sxs-lookup"><span data-stu-id="7298d-109">The Remove-AzIotSecuritySolution cmdlet deletes a specific iot security solution.</span></span> <span data-ttu-id="7298d-110">IoT-säkerhetslösningen samlar in säkerhets data från IoT-enheter och IoT Hub för att förhindra och upptäcka hot.</span><span class="sxs-lookup"><span data-stu-id="7298d-110">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="7298d-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7298d-111">EXAMPLES</span></span>

### <span data-ttu-id="7298d-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7298d-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="7298d-113">Delete IoT Security Solution "testprov" med resurs gruppen "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="7298d-113">Delete IoT security solution "MySample" with resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="7298d-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7298d-114">PARAMETERS</span></span>

### <span data-ttu-id="7298d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7298d-115">-DefaultProfile</span></span>
<span data-ttu-id="7298d-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7298d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7298d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7298d-117">-InputObject</span></span>
<span data-ttu-id="7298d-118">Indatavärdet.</span><span class="sxs-lookup"><span data-stu-id="7298d-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7298d-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="7298d-119">-Name</span></span>
<span data-ttu-id="7298d-120">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="7298d-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7298d-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7298d-121">-PassThru</span></span>
<span data-ttu-id="7298d-122">Returnera om åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="7298d-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="7298d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7298d-123">-ResourceGroupName</span></span>
<span data-ttu-id="7298d-124">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="7298d-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7298d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7298d-125">-ResourceId</span></span>
<span data-ttu-id="7298d-126">ID för den säkerhets resurs som du vill starta kommandot på.</span><span class="sxs-lookup"><span data-stu-id="7298d-126">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7298d-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7298d-127">-Confirm</span></span>
<span data-ttu-id="7298d-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7298d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7298d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7298d-129">-WhatIf</span></span>
<span data-ttu-id="7298d-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7298d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7298d-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7298d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7298d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7298d-132">CommonParameters</span></span>
<span data-ttu-id="7298d-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7298d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7298d-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7298d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7298d-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7298d-135">INPUTS</span></span>

### <span data-ttu-id="7298d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="7298d-136">System.String</span></span>

### <span data-ttu-id="7298d-137">Microsoft. Azure. commands. Security. Models. IotSecuritySolutions. PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="7298d-137">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="7298d-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7298d-138">OUTPUTS</span></span>

### <span data-ttu-id="7298d-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7298d-139">System.Boolean</span></span>

## <span data-ttu-id="7298d-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7298d-140">NOTES</span></span>

## <span data-ttu-id="7298d-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7298d-141">RELATED LINKS</span></span>
