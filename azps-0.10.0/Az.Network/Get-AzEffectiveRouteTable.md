---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectiveroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzEffectiveRouteTable.md
ms.openlocfilehash: 37c9827f2af970c0c376c31f4d67ba7723e02e99
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922298"
---
# <span data-ttu-id="215bb-101">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="215bb-101">Get-AzEffectiveRouteTable</span></span>

## <span data-ttu-id="215bb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="215bb-102">SYNOPSIS</span></span>
<span data-ttu-id="215bb-103">Hämtar tabellen med giltighets vägar för ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="215bb-103">Gets the effective route table of a network interface.</span></span>

## <span data-ttu-id="215bb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="215bb-104">SYNTAX</span></span>

```
Get-AzEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="215bb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="215bb-105">DESCRIPTION</span></span>
<span data-ttu-id="215bb-106">Cmdleten **Get-AzEffectiveRouteTable** returnerar den giltiga routningstabellen som tillämpas på ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="215bb-106">The **Get-AzEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="215bb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="215bb-107">EXAMPLES</span></span>

### <span data-ttu-id="215bb-108">Exempel 1: Hämta tabellen med effektiva vägar i ett nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="215bb-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="215bb-109">Det här kommandot hämtar den giltiga routningstabellen som är associerad med nätverks gränssnittet med namnet MyNetworkInterface i resurs gruppen med namnet MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="215bb-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="215bb-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="215bb-110">PARAMETERS</span></span>

### <span data-ttu-id="215bb-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="215bb-111">-AsJob</span></span>
<span data-ttu-id="215bb-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="215bb-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="215bb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="215bb-113">-DefaultProfile</span></span>
<span data-ttu-id="215bb-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="215bb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="215bb-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="215bb-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="215bb-116">Ange namnet på ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="215bb-116">Specified the name of a network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="215bb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="215bb-117">-ResourceGroupName</span></span>
<span data-ttu-id="215bb-118">Anger resurs gruppen för ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="215bb-118">Specifies the resource group of a network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="215bb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="215bb-119">CommonParameters</span></span>
<span data-ttu-id="215bb-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="215bb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="215bb-121">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="215bb-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="215bb-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="215bb-122">INPUTS</span></span>

## <span data-ttu-id="215bb-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="215bb-123">OUTPUTS</span></span>

### <span data-ttu-id="215bb-124">Microsoft. Azure. commands. Networks. Models. PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="215bb-124">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="215bb-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="215bb-125">NOTES</span></span>

## <span data-ttu-id="215bb-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="215bb-126">RELATED LINKS</span></span>

[<span data-ttu-id="215bb-127">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="215bb-127">Get-AzEffectiveNetworkSecurityGroup</span></span>](./Get-AzEffectiveNetworkSecurityGroup.md)


