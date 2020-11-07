---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteFilter.md
ms.openlocfilehash: 80887622c5a9dbc3c6ddf544d435974b8212d9ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755994"
---
# <span data-ttu-id="d18db-101">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="d18db-101">Get-AzureRmRouteFilter</span></span>

## <span data-ttu-id="d18db-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d18db-102">SYNOPSIS</span></span>
<span data-ttu-id="d18db-103">{{Fyll i sammanfattningen}}</span><span class="sxs-lookup"><span data-stu-id="d18db-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d18db-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d18db-104">SYNTAX</span></span>

### <span data-ttu-id="d18db-105">Noexpandering</span><span class="sxs-lookup"><span data-stu-id="d18db-105">NoExpand</span></span>
```
Get-AzureRmRouteFilter [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d18db-106">Byggnad</span><span class="sxs-lookup"><span data-stu-id="d18db-106">Expand</span></span>
```
Get-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d18db-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d18db-107">DESCRIPTION</span></span>
<span data-ttu-id="d18db-108">{{Fyll i beskrivningen}}</span><span class="sxs-lookup"><span data-stu-id="d18db-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="d18db-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d18db-109">EXAMPLES</span></span>

### <span data-ttu-id="d18db-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d18db-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="d18db-111">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="d18db-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="d18db-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d18db-112">PARAMETERS</span></span>

### <span data-ttu-id="d18db-113">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="d18db-113">-ExpandResource</span></span>
<span data-ttu-id="d18db-114">Resurs referensen som ska expanderas.</span><span class="sxs-lookup"><span data-stu-id="d18db-114">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d18db-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="d18db-115">-Name</span></span>
<span data-ttu-id="d18db-116">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="d18db-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d18db-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d18db-117">-ResourceGroupName</span></span>
<span data-ttu-id="d18db-118">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="d18db-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d18db-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d18db-119">-DefaultProfile</span></span>
<span data-ttu-id="d18db-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d18db-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d18db-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d18db-121">CommonParameters</span></span>
<span data-ttu-id="d18db-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d18db-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d18db-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d18db-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d18db-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d18db-124">INPUTS</span></span>

### <span data-ttu-id="d18db-125">System. String</span><span class="sxs-lookup"><span data-stu-id="d18db-125">System.String</span></span>

## <span data-ttu-id="d18db-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d18db-126">OUTPUTS</span></span>

### <span data-ttu-id="d18db-127">Microsoft. Azure. commands. Networks. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="d18db-127">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="d18db-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d18db-128">NOTES</span></span>

## <span data-ttu-id="d18db-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d18db-129">RELATED LINKS</span></span>

