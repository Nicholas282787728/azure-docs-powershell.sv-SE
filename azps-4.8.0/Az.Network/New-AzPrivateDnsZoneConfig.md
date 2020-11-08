---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatednszoneconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
ms.openlocfilehash: b80889f1838945f6ba119f539c5badd59b43de61
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102699"
---
# <span data-ttu-id="13759-101">New-AzPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="13759-101">New-AzPrivateDnsZoneConfig</span></span>

## <span data-ttu-id="13759-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="13759-102">SYNOPSIS</span></span>
<span data-ttu-id="13759-103">Skapar DNS-zonöverföringar för gruppen privata DNS-zoner.</span><span class="sxs-lookup"><span data-stu-id="13759-103">Creates DNS zone configuration of the private dns zone group.</span></span>

## <span data-ttu-id="13759-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="13759-104">SYNTAX</span></span>

```
New-AzPrivateDnsZoneConfig -Name <String> [-PrivateDnsZoneId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13759-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="13759-105">DESCRIPTION</span></span>
<span data-ttu-id="13759-106">Med **New-AzPrivateDnsZoneConfig** cmdlet kan du skapa ett nytt konfigurations objekt för DNS-zon som kommer att anges i DNS-zonfilen.</span><span class="sxs-lookup"><span data-stu-id="13759-106">The **New-AzPrivateDnsZoneConfig** cmdlet enables you to create a new DNS zone configuration object which will be set on DNS zone group.</span></span>

## <span data-ttu-id="13759-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="13759-107">EXAMPLES</span></span>

### <span data-ttu-id="13759-108">Skapar konfiguration för DNS-zoner</span><span class="sxs-lookup"><span data-stu-id="13759-108">Creates DNS zone configuration</span></span>
```powershell
PS C:\> $dnsZone = New-AzPrivateDnsZone -ResourceGroupName "rg" -Name "test.vault.azure.com"
PS C:\> $config = New-AzPrivateDnsZoneConfig -Name "test-vault-azure-com" -PrivateDnsZoneId $dnsZone.ResourceId
```

<span data-ttu-id="13759-109">Exemplet ovan skapar DNS Zone och skapar sedan DNS Zone-konfigurering.</span><span class="sxs-lookup"><span data-stu-id="13759-109">The above example creates DNS zone and then creates DNS zone configuration.</span></span> <span data-ttu-id="13759-110">`New-AzPrivateDnsZone` cmdleten bevaras av modul AZ. PrivateDns.</span><span class="sxs-lookup"><span data-stu-id="13759-110">`New-AzPrivateDnsZone` cmdlet is proveded by module Az.PrivateDns.</span></span>

## <span data-ttu-id="13759-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="13759-111">PARAMETERS</span></span>

### <span data-ttu-id="13759-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13759-112">-DefaultProfile</span></span>
<span data-ttu-id="13759-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="13759-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13759-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="13759-114">-Name</span></span>
<span data-ttu-id="13759-115">Namnet på resursen som är unik i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="13759-115">Name of the resource that is unique within a resource group.</span></span>
<span data-ttu-id="13759-116">Det här namnet kan användas för att komma åt resursen.</span><span class="sxs-lookup"><span data-stu-id="13759-116">This name can be used to access the resource.</span></span>

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

### <span data-ttu-id="13759-117">-PrivateDnsZoneId</span><span class="sxs-lookup"><span data-stu-id="13759-117">-PrivateDnsZoneId</span></span>
<span data-ttu-id="13759-118">Resurs-ID för den privata DNS-zonen.</span><span class="sxs-lookup"><span data-stu-id="13759-118">The resource id of the private dns zone.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13759-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13759-119">CommonParameters</span></span>
<span data-ttu-id="13759-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13759-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13759-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13759-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13759-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="13759-122">INPUTS</span></span>

### <span data-ttu-id="13759-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="13759-123">None</span></span>

## <span data-ttu-id="13759-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="13759-124">OUTPUTS</span></span>

### <span data-ttu-id="13759-125">Microsoft. Azure. commands. Networks. Models. PSPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="13759-125">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig</span></span>

## <span data-ttu-id="13759-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="13759-126">NOTES</span></span>

## <span data-ttu-id="13759-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="13759-127">RELATED LINKS</span></span>
