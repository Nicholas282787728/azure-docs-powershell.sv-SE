---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 1CA26790-C791-4BFD-B986-70F28E3B095B
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActionGroup.md
ms.openlocfilehash: 90bd9c7943e6e788d81f8ddec85513676afade23
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524025"
---
# <span data-ttu-id="b7cd9-101">Get-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="b7cd9-101">Get-AzActionGroup</span></span>

## <span data-ttu-id="b7cd9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b7cd9-102">SYNOPSIS</span></span>
<span data-ttu-id="b7cd9-103">Hämtar åtgärds grupper.</span><span class="sxs-lookup"><span data-stu-id="b7cd9-103">Gets action group(s).</span></span>

## <span data-ttu-id="b7cd9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b7cd9-104">SYNTAX</span></span>

### <span data-ttu-id="b7cd9-105">BySubscriptionOrResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="b7cd9-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzActionGroup [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7cd9-106">ByName</span><span class="sxs-lookup"><span data-stu-id="b7cd9-106">ByName</span></span>
```
Get-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b7cd9-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b7cd9-107">DESCRIPTION</span></span>
<span data-ttu-id="b7cd9-108">Cmdleten **Get-AzActionGroup** hämtar en eller flera åtgärds grupper.</span><span class="sxs-lookup"><span data-stu-id="b7cd9-108">The **Get-AzActionGroup** cmdlet gets one or more action groups.</span></span>

## <span data-ttu-id="b7cd9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b7cd9-109">EXAMPLES</span></span>

### <span data-ttu-id="b7cd9-110">Exempel 1: Hämta en åtgärds grupp efter abonnemangs-ID</span><span class="sxs-lookup"><span data-stu-id="b7cd9-110">Example 1: Get an action group by subscription ID</span></span>
```
PS C:\>Get-AzActionGroup
```

<span data-ttu-id="b7cd9-111">Det här kommandot listar alla åtgärds grupper för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="b7cd9-111">This command lists all the action group for the current subscription.</span></span>

### <span data-ttu-id="b7cd9-112">Exempel 2: Hämta åtgärds grupper för den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="b7cd9-112">Example 2: Get action groups for the given resource group</span></span>
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts"
```

<span data-ttu-id="b7cd9-113">Det här kommandot visar åtgärds grupper för den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b7cd9-113">This command lists action groups for the given resource group.</span></span>

### <span data-ttu-id="b7cd9-114">Exempel 3: Hämta en åtgärds grupp.</span><span class="sxs-lookup"><span data-stu-id="b7cd9-114">Example 3: Get an action group.</span></span>
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts" -Name "actionGroup1"
```

<span data-ttu-id="b7cd9-115">Det här kommandot listar en (en lista med en enda element)-åtgärds grupp.</span><span class="sxs-lookup"><span data-stu-id="b7cd9-115">This command lists one (a list with a single element) action group.</span></span>

## <span data-ttu-id="b7cd9-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b7cd9-116">PARAMETERS</span></span>

### <span data-ttu-id="b7cd9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7cd9-117">-DefaultProfile</span></span>
<span data-ttu-id="b7cd9-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b7cd9-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7cd9-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="b7cd9-119">-Name</span></span>
<span data-ttu-id="b7cd9-120">Namnet på åtgärds gruppen.</span><span class="sxs-lookup"><span data-stu-id="b7cd9-120">The name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7cd9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7cd9-121">-ResourceGroupName</span></span>
<span data-ttu-id="b7cd9-122">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="b7cd9-122">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionOrResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7cd9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7cd9-123">CommonParameters</span></span>
<span data-ttu-id="b7cd9-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7cd9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7cd9-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7cd9-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7cd9-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b7cd9-126">INPUTS</span></span>

### <span data-ttu-id="b7cd9-127">System. String</span><span class="sxs-lookup"><span data-stu-id="b7cd9-127">System.String</span></span>

## <span data-ttu-id="b7cd9-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b7cd9-128">OUTPUTS</span></span>

### <span data-ttu-id="b7cd9-129">Microsoft. Azure. commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="b7cd9-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="b7cd9-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b7cd9-130">NOTES</span></span>

## <span data-ttu-id="b7cd9-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b7cd9-131">RELATED LINKS</span></span>

<span data-ttu-id="b7cd9-132">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md) 
 [New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="b7cd9-132">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)
[New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span></span>
