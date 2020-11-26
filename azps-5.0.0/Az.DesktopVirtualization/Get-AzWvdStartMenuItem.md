---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdstartmenuitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
ms.openlocfilehash: d4390f7de7b9fb91cf998050f192a3ba282e9585
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320044"
---
# <span data-ttu-id="deb5e-101">Get-AzWvdStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="deb5e-101">Get-AzWvdStartMenuItem</span></span>

## <span data-ttu-id="deb5e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="deb5e-102">SYNOPSIS</span></span>
<span data-ttu-id="deb5e-103">Lista över objekt på Start-menyn i den angivna program gruppen.</span><span class="sxs-lookup"><span data-stu-id="deb5e-103">List start menu items in the given application group.</span></span>

## <span data-ttu-id="deb5e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="deb5e-104">SYNTAX</span></span>

```
Get-AzWvdStartMenuItem -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="deb5e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="deb5e-105">DESCRIPTION</span></span>
<span data-ttu-id="deb5e-106">Lista över objekt på Start-menyn i den angivna program gruppen.</span><span class="sxs-lookup"><span data-stu-id="deb5e-106">List start menu items in the given application group.</span></span>

## <span data-ttu-id="deb5e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="deb5e-107">EXAMPLES</span></span>

### <span data-ttu-id="deb5e-108">Exempel 2: lista objekt på Start-menyn i Windows Virtual Desktop</span><span class="sxs-lookup"><span data-stu-id="deb5e-108">Example 2: List Windows Virtual Desktop Start Menu Items</span></span>
```powershell
PS C:\> Get-AzWvdStartMenuItem -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                                Type
----                                                ----
ApplicationGroupName/Character Map                  Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Defragment and Optimize Drives Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Disk Cleanup                   Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Internet Explorer              Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
```

<span data-ttu-id="deb5e-109">Det här kommandot visar objekt på Start-menyn i en applicaton-grupp.</span><span class="sxs-lookup"><span data-stu-id="deb5e-109">This command Lists Windows Virtual Desktop Start Menu Items in an applicaton Group.</span></span>

## <span data-ttu-id="deb5e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="deb5e-110">PARAMETERS</span></span>

### <span data-ttu-id="deb5e-111">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="deb5e-111">-ApplicationGroupName</span></span>
<span data-ttu-id="deb5e-112">Namnet på program gruppen</span><span class="sxs-lookup"><span data-stu-id="deb5e-112">The name of the application group</span></span>

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

### <span data-ttu-id="deb5e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="deb5e-113">-DefaultProfile</span></span>
<span data-ttu-id="deb5e-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="deb5e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="deb5e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="deb5e-115">-ResourceGroupName</span></span>
<span data-ttu-id="deb5e-116">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="deb5e-116">The name of the resource group.</span></span>
<span data-ttu-id="deb5e-117">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="deb5e-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="deb5e-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="deb5e-118">-SubscriptionId</span></span>
<span data-ttu-id="deb5e-119">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="deb5e-119">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deb5e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deb5e-120">CommonParameters</span></span>
<span data-ttu-id="deb5e-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="deb5e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deb5e-122">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="deb5e-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deb5e-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="deb5e-123">INPUTS</span></span>

## <span data-ttu-id="deb5e-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="deb5e-124">OUTPUTS</span></span>

### <span data-ttu-id="deb5e-125">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. Api20191210Preview. IStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="deb5e-125">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IStartMenuItem</span></span>

## <span data-ttu-id="deb5e-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="deb5e-126">NOTES</span></span>

<span data-ttu-id="deb5e-127">ALIAS</span><span class="sxs-lookup"><span data-stu-id="deb5e-127">ALIASES</span></span>

## <span data-ttu-id="deb5e-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="deb5e-128">RELATED LINKS</span></span>
