---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 1CA26790-C791-4BFD-B986-70F28E3B095B
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActionGroup.md
ms.openlocfilehash: c297198a1e49b93d498c136d1cb099d2068d24db
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092732"
---
# <span data-ttu-id="82daa-101">Get-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="82daa-101">Get-AzActionGroup</span></span>

## <span data-ttu-id="82daa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="82daa-102">SYNOPSIS</span></span>
<span data-ttu-id="82daa-103">Hämtar åtgärds grupper.</span><span class="sxs-lookup"><span data-stu-id="82daa-103">Gets action group(s).</span></span>

## <span data-ttu-id="82daa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="82daa-104">SYNTAX</span></span>

### <span data-ttu-id="82daa-105">BySubscriptionOrResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="82daa-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzActionGroup [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82daa-106">ByName</span><span class="sxs-lookup"><span data-stu-id="82daa-106">ByName</span></span>
```
Get-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="82daa-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="82daa-107">DESCRIPTION</span></span>
<span data-ttu-id="82daa-108">Cmdleten **Get-AzActionGroup** hämtar en eller flera åtgärds grupper.</span><span class="sxs-lookup"><span data-stu-id="82daa-108">The **Get-AzActionGroup** cmdlet gets one or more action groups.</span></span>

## <span data-ttu-id="82daa-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="82daa-109">EXAMPLES</span></span>

### <span data-ttu-id="82daa-110">Exempel 1: Hämta en åtgärds grupp efter abonnemangs-ID</span><span class="sxs-lookup"><span data-stu-id="82daa-110">Example 1: Get an action group by subscription ID</span></span>
```
PS C:\>Get-AzActionGroup
```

<span data-ttu-id="82daa-111">Det här kommandot listar alla åtgärds grupper för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="82daa-111">This command lists all the action group for the current subscription.</span></span>

### <span data-ttu-id="82daa-112">Exempel 2: Hämta åtgärds grupper för den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="82daa-112">Example 2: Get action groups for the given resource group</span></span>
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts"
```

<span data-ttu-id="82daa-113">Det här kommandot visar åtgärds grupper för den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="82daa-113">This command lists action groups for the given resource group.</span></span>

### <span data-ttu-id="82daa-114">Exempel 3: Hämta en åtgärds grupp.</span><span class="sxs-lookup"><span data-stu-id="82daa-114">Example 3: Get an action group.</span></span>
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts" -Name "actionGroup1"
```

<span data-ttu-id="82daa-115">Det här kommandot listar en (en lista med en enda element)-åtgärds grupp.</span><span class="sxs-lookup"><span data-stu-id="82daa-115">This command lists one (a list with a single element) action group.</span></span>

## <span data-ttu-id="82daa-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="82daa-116">PARAMETERS</span></span>

### <span data-ttu-id="82daa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82daa-117">-DefaultProfile</span></span>
<span data-ttu-id="82daa-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="82daa-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82daa-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="82daa-119">-Name</span></span>
<span data-ttu-id="82daa-120">Namnet på åtgärds gruppen.</span><span class="sxs-lookup"><span data-stu-id="82daa-120">The name of the action group.</span></span>

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

### <span data-ttu-id="82daa-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82daa-121">-ResourceGroupName</span></span>
<span data-ttu-id="82daa-122">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="82daa-122">The resource group name</span></span>

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

### <span data-ttu-id="82daa-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82daa-123">CommonParameters</span></span>
<span data-ttu-id="82daa-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82daa-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82daa-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="82daa-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82daa-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="82daa-126">INPUTS</span></span>

### <span data-ttu-id="82daa-127">System. String</span><span class="sxs-lookup"><span data-stu-id="82daa-127">System.String</span></span>

## <span data-ttu-id="82daa-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="82daa-128">OUTPUTS</span></span>

### <span data-ttu-id="82daa-129">Microsoft. Azure. commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="82daa-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="82daa-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="82daa-130">NOTES</span></span>

## <span data-ttu-id="82daa-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="82daa-131">RELATED LINKS</span></span>

<span data-ttu-id="82daa-132">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md) 
 [New-AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="82daa-132">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)
[New-AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
