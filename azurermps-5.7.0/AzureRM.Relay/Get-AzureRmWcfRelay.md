---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmWcfRelay.md
ms.openlocfilehash: 88d2c8f7b0bcab3faad6368070606b8a36948343
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583080"
---
# <span data-ttu-id="31bb8-101">Get-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="31bb8-101">Get-AzureRmWcfRelay</span></span>

## <span data-ttu-id="31bb8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="31bb8-102">SYNOPSIS</span></span>
<span data-ttu-id="31bb8-103">Returnerar en beskrivning för den angivna WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="31bb8-103">Returns a description for the specified WcfRelay.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31bb8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="31bb8-104">SYNTAX</span></span>

```
Get-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31bb8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="31bb8-105">DESCRIPTION</span></span>
<span data-ttu-id="31bb8-106">Cmdleten **Get-AzureRmWcfRelay** returnerar en beskrivning av angiven WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="31bb8-106">The **Get-AzureRmWcfRelay** cmdlet returns a description of the specified WcfRelay.</span></span>

## <span data-ttu-id="31bb8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="31bb8-107">EXAMPLES</span></span>

### <span data-ttu-id="31bb8-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="31bb8-108">Example 1</span></span>
```
PS C:\> Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="31bb8-109">Returnerar beskrivningen av WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="31bb8-109">Returns the description of the WcfRelay.</span></span> 

## <span data-ttu-id="31bb8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="31bb8-110">PARAMETERS</span></span>

### <span data-ttu-id="31bb8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31bb8-111">-DefaultProfile</span></span>
<span data-ttu-id="31bb8-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="31bb8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31bb8-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="31bb8-113">-Name</span></span>
<span data-ttu-id="31bb8-114">WcfRelay namn.</span><span class="sxs-lookup"><span data-stu-id="31bb8-114">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31bb8-115">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="31bb8-115">-Namespace</span></span>
<span data-ttu-id="31bb8-116">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="31bb8-116">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31bb8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31bb8-117">-ResourceGroupName</span></span>
<span data-ttu-id="31bb8-118">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="31bb8-118">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31bb8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31bb8-119">CommonParameters</span></span>
<span data-ttu-id="31bb8-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31bb8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31bb8-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31bb8-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31bb8-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="31bb8-122">INPUTS</span></span>

### <span data-ttu-id="31bb8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31bb8-123">-ResourceGroupName</span></span>
 <span data-ttu-id="31bb8-124">System. String</span><span class="sxs-lookup"><span data-stu-id="31bb8-124">System.String</span></span>
 

### <span data-ttu-id="31bb8-125">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="31bb8-125">-Namespace</span></span>
 <span data-ttu-id="31bb8-126">System. String</span><span class="sxs-lookup"><span data-stu-id="31bb8-126">System.String</span></span>
 

### <span data-ttu-id="31bb8-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="31bb8-127">-Name</span></span>
 <span data-ttu-id="31bb8-128">System. String</span><span class="sxs-lookup"><span data-stu-id="31bb8-128">System.String</span></span> 

## <span data-ttu-id="31bb8-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="31bb8-129">OUTPUTS</span></span>

### <span data-ttu-id="31bb8-130">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Relay. Models. WcfRelayAttributes, Microsoft. Azure. commands. Relay, version = 0.1.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="31bb8-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="31bb8-131">RelayType: NetTcp CreatedAt: 4/12/2017 2:23:08 AM UpdatedAt: 4/12/2017 2:23:08 AM ListenerCount: 0 RequiresClientAuthorization: true RequiresTransportSecurity: true IsDynamic: false UserMetadata: User meta data-ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/W cfRelays/TestWCFRelay1 namn: TestWCFRelay1: Microsoft. Relay/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="31bb8-131">RelayType                   : NetTcp CreatedAt                   : 4/12/2017 2:23:08 AM UpdatedAt                   : 4/12/2017 2:23:08 AM ListenerCount               : 0 RequiresClientAuthorization : True RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : User Meta data Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/W cfRelays/TestWCFRelay1 Name                        : TestWCFRelay1 Type                        : Microsoft.Relay/WcfRelays</span></span>

## <span data-ttu-id="31bb8-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="31bb8-132">NOTES</span></span>

## <span data-ttu-id="31bb8-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="31bb8-133">RELATED LINKS</span></span>

