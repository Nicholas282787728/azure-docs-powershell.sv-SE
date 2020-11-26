---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/register-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Register-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Register-AzWvdApplicationGroup.md
ms.openlocfilehash: 874cc587bff418bf0d6846fe39bdf7d10c42d7dd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320007"
---
# <span data-ttu-id="c3679-101">Register-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="c3679-101">Register-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="c3679-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c3679-102">SYNOPSIS</span></span>
<span data-ttu-id="c3679-103">Registrera en Windows-grupp för virtuella skriv bord.</span><span class="sxs-lookup"><span data-stu-id="c3679-103">Register a Windows virtual desktop application group.</span></span>

## <span data-ttu-id="c3679-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c3679-104">SYNTAX</span></span>

```
Register-AzWvdApplicationGroup -ApplicationGroupPath <String> -ResourceGroupName <String>
 -WorkspaceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="c3679-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c3679-105">DESCRIPTION</span></span>
<span data-ttu-id="c3679-106">Registrera en Windows-grupp för virtuella skriv bord.</span><span class="sxs-lookup"><span data-stu-id="c3679-106">Register a Windows virtual desktop application group.</span></span>

## <span data-ttu-id="c3679-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c3679-107">EXAMPLES</span></span>

### <span data-ttu-id="c3679-108">Exempel 1: registrera en Windows Virtual Desktop-gruppgrupp</span><span class="sxs-lookup"><span data-stu-id="c3679-108">Example 1: Register a Windows Virtual Desktop Application Group</span></span>
```powershell
PS C:\> Register-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                                    -WorkspaceName WorkspaceName `
                                    -ApplicationGroupPath '/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="c3679-109">Det här kommandot registrerar en Windows Virtual Desktop-programgrupp på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="c3679-109">This command registers a Windows Virtual Desktop Application Group to a Workspace.</span></span>

## <span data-ttu-id="c3679-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c3679-110">PARAMETERS</span></span>

### <span data-ttu-id="c3679-111">-ApplicationGroupPath</span><span class="sxs-lookup"><span data-stu-id="c3679-111">-ApplicationGroupPath</span></span>
<span data-ttu-id="c3679-112">ApplicationGroupPath sökväg</span><span class="sxs-lookup"><span data-stu-id="c3679-112">ApplicationGroupPath Path</span></span>

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

### <span data-ttu-id="c3679-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3679-113">-DefaultProfile</span></span>
<span data-ttu-id="c3679-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c3679-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3679-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3679-115">-ResourceGroupName</span></span>
<span data-ttu-id="c3679-116">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="c3679-116">Resource Group Name</span></span>

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

### <span data-ttu-id="c3679-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c3679-117">-SubscriptionId</span></span>
<span data-ttu-id="c3679-118">Abonnemangs-ID</span><span class="sxs-lookup"><span data-stu-id="c3679-118">Subscription Id</span></span>

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

### <span data-ttu-id="c3679-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c3679-119">-WorkspaceName</span></span>
<span data-ttu-id="c3679-120">Namn på arbets ytan</span><span class="sxs-lookup"><span data-stu-id="c3679-120">Workspace Name</span></span>

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

### <span data-ttu-id="c3679-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c3679-121">-Confirm</span></span>
<span data-ttu-id="c3679-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c3679-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3679-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3679-123">-WhatIf</span></span>
<span data-ttu-id="c3679-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c3679-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3679-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c3679-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3679-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3679-126">CommonParameters</span></span>
<span data-ttu-id="c3679-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3679-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3679-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c3679-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3679-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c3679-129">INPUTS</span></span>

## <span data-ttu-id="c3679-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c3679-130">OUTPUTS</span></span>

### <span data-ttu-id="c3679-131">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. Api20191210Preview. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="c3679-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="c3679-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c3679-132">NOTES</span></span>

<span data-ttu-id="c3679-133">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c3679-133">ALIASES</span></span>

## <span data-ttu-id="c3679-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c3679-134">RELATED LINKS</span></span>
