---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/unregister-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Unregister-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Unregister-AzWvdApplicationGroup.md
ms.openlocfilehash: 0533864f3fd16e9810e837629782b767fbdc0435
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426336"
---
# <span data-ttu-id="7d37d-101">Unregister-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="7d37d-101">Unregister-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="7d37d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7d37d-102">SYNOPSIS</span></span>
<span data-ttu-id="7d37d-103">Avregistrera program gruppen virtuellt skriv bord i Windows.</span><span class="sxs-lookup"><span data-stu-id="7d37d-103">Unregister the Windows virtual desktop application group.</span></span>

## <span data-ttu-id="7d37d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7d37d-104">SYNTAX</span></span>

```
Unregister-AzWvdApplicationGroup -ApplicationGroupPath <String> -ResourceGroupName <String>
 -WorkspaceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="7d37d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7d37d-105">DESCRIPTION</span></span>
<span data-ttu-id="7d37d-106">Avregistrera program gruppen virtuellt skriv bord i Windows.</span><span class="sxs-lookup"><span data-stu-id="7d37d-106">Unregister the Windows virtual desktop application group.</span></span>

## <span data-ttu-id="7d37d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7d37d-107">EXAMPLES</span></span>

### <span data-ttu-id="7d37d-108">Exempel 1: avregistrera en Windows Virtual Desktop-gruppgrupp</span><span class="sxs-lookup"><span data-stu-id="7d37d-108">Example 1: Unregister a Windows Virtual Desktop Application Group</span></span>
```powershell
PS C:\> Unregister-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                                    -WorkspaceName WorkspaceName `
                                    -ApplicationGroupPath '/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="7d37d-109">Det här kommandot avregistrerar en Windows Virtual Desktop-gruppprogram grupp på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="7d37d-109">This command unregisters a Windows Virtual Desktop Application Group to a Workspace.</span></span>

## <span data-ttu-id="7d37d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7d37d-110">PARAMETERS</span></span>

### <span data-ttu-id="7d37d-111">-ApplicationGroupPath</span><span class="sxs-lookup"><span data-stu-id="7d37d-111">-ApplicationGroupPath</span></span>
<span data-ttu-id="7d37d-112">ResourceGroupName sökväg</span><span class="sxs-lookup"><span data-stu-id="7d37d-112">ResourceGroupName Path</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d37d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d37d-113">-DefaultProfile</span></span>
<span data-ttu-id="7d37d-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7d37d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d37d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d37d-115">-ResourceGroupName</span></span>
<span data-ttu-id="7d37d-116">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="7d37d-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d37d-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7d37d-117">-SubscriptionId</span></span>
<span data-ttu-id="7d37d-118">Abonnemangs-ID</span><span class="sxs-lookup"><span data-stu-id="7d37d-118">Subscription Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d37d-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7d37d-119">-WorkspaceName</span></span>
<span data-ttu-id="7d37d-120">Namn på arbets ytan</span><span class="sxs-lookup"><span data-stu-id="7d37d-120">Workspace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d37d-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7d37d-121">-Confirm</span></span>
<span data-ttu-id="7d37d-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7d37d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d37d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d37d-123">-WhatIf</span></span>
<span data-ttu-id="7d37d-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7d37d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d37d-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7d37d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d37d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d37d-126">CommonParameters</span></span>
<span data-ttu-id="7d37d-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d37d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d37d-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7d37d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d37d-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7d37d-129">INPUTS</span></span>

## <span data-ttu-id="7d37d-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7d37d-130">OUTPUTS</span></span>

### <span data-ttu-id="7d37d-131">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. Api20191210Preview. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="7d37d-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="7d37d-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7d37d-132">NOTES</span></span>

<span data-ttu-id="7d37d-133">ALIAS</span><span class="sxs-lookup"><span data-stu-id="7d37d-133">ALIASES</span></span>

## <span data-ttu-id="7d37d-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7d37d-134">RELATED LINKS</span></span>

