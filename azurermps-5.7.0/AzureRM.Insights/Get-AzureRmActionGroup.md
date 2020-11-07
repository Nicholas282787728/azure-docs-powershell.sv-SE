---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 1CA26790-C791-4BFD-B986-70F28E3B095B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActionGroup.md
ms.openlocfilehash: 08785d6fe4afe918ca593eeff7ee7aa9cfbfe578
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756506"
---
# <span data-ttu-id="8684f-101">Get-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="8684f-101">Get-AzureRmActionGroup</span></span>

## <span data-ttu-id="8684f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8684f-102">SYNOPSIS</span></span>
<span data-ttu-id="8684f-103">Hämtar åtgärds grupper.</span><span class="sxs-lookup"><span data-stu-id="8684f-103">Gets action group(s).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8684f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8684f-104">SYNTAX</span></span>

### <span data-ttu-id="8684f-105">BySubscriptionOrResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="8684f-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzureRmActionGroup [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8684f-106">ByName</span><span class="sxs-lookup"><span data-stu-id="8684f-106">ByName</span></span>
```
Get-AzureRmActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8684f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8684f-107">DESCRIPTION</span></span>
<span data-ttu-id="8684f-108">Cmdleten **Get-AzureRmActionGroup** hämtar en eller flera åtgärds grupper.</span><span class="sxs-lookup"><span data-stu-id="8684f-108">The **Get-AzureRmActionGroup** cmdlet gets one or more action groups.</span></span>

## <span data-ttu-id="8684f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8684f-109">EXAMPLES</span></span>

### <span data-ttu-id="8684f-110">Exempel 1: Hämta en åtgärds grupp efter abonnemangs-ID</span><span class="sxs-lookup"><span data-stu-id="8684f-110">Example 1: Get an action group by subscription ID</span></span>
```
PS C:\>Get-AzureRmActionGroup
```

<span data-ttu-id="8684f-111">Det här kommandot listar alla åtgärds grupper för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="8684f-111">This command lists all the action group for the current subscription.</span></span>

### <span data-ttu-id="8684f-112">Exempel 2: Hämta åtgärds grupper för den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="8684f-112">Example 2: Get action groups for the given resource group</span></span>
```
PS C:\>Get-AzureRmActionGroup -ResourceGroup "Default-activityLogAlerts"
```

<span data-ttu-id="8684f-113">Det här kommandot visar åtgärds grupper för den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="8684f-113">This command lists action groups for the given resource group.</span></span>

### <span data-ttu-id="8684f-114">Exempel 3: Hämta en åtgärds grupp.</span><span class="sxs-lookup"><span data-stu-id="8684f-114">Example 3: Get an action group.</span></span>
```
PS C:\>Get-AzureRmActionGroup -ResourceGroup "Default-activityLogAlerts" -Name "actionGroup1"
```

<span data-ttu-id="8684f-115">Det här kommandot listar en (en lista med en enda element)-åtgärds grupp.</span><span class="sxs-lookup"><span data-stu-id="8684f-115">This command lists one (a list with a single element) action group.</span></span>

## <span data-ttu-id="8684f-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8684f-116">PARAMETERS</span></span>

### <span data-ttu-id="8684f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8684f-117">-DefaultProfile</span></span>
<span data-ttu-id="8684f-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="8684f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8684f-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="8684f-119">-Name</span></span>
<span data-ttu-id="8684f-120">Namnet på åtgärds gruppen.</span><span class="sxs-lookup"><span data-stu-id="8684f-120">The name of the action group.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8684f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8684f-121">-ResourceGroupName</span></span>
<span data-ttu-id="8684f-122">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="8684f-122">The resource group name</span></span>

```yaml
Type: String
Parameter Sets: BySubscriptionOrResourceGroup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8684f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8684f-123">CommonParameters</span></span>
<span data-ttu-id="8684f-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8684f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8684f-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8684f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8684f-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8684f-126">INPUTS</span></span>

### <span data-ttu-id="8684f-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="8684f-127">None</span></span>

## <span data-ttu-id="8684f-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8684f-128">OUTPUTS</span></span>

### <span data-ttu-id="8684f-129"><system. Collections. Generic. list ' 1 [Microsoft. Azure. commands. Insights. OutputClasses. PSActionGroupResource]</span><span class="sxs-lookup"><span data-stu-id="8684f-129"><System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource]</span></span>

### <span data-ttu-id="8684f-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="8684f-130">None</span></span>

## <span data-ttu-id="8684f-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8684f-131">NOTES</span></span>

## <span data-ttu-id="8684f-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8684f-132">RELATED LINKS</span></span>

<span data-ttu-id="8684f-133">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md) 
 [New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="8684f-133">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
