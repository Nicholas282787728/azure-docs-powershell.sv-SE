---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: dc90facde7d79b308ff456be9f2df1b8c087a4a6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98527683"
---
# <span data-ttu-id="9c49e-101">Get-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="9c49e-101">Get-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="9c49e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9c49e-102">SYNOPSIS</span></span>
<span data-ttu-id="9c49e-103">Hämtar en privat DNS-zonfil</span><span class="sxs-lookup"><span data-stu-id="9c49e-103">Gets private DNS zone group</span></span>

## <span data-ttu-id="9c49e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9c49e-104">SYNTAX</span></span>

### <span data-ttu-id="9c49e-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="9c49e-105">List (Default)</span></span>
```
Get-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c49e-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="9c49e-106">GetByName</span></span>
```
Get-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c49e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9c49e-107">DESCRIPTION</span></span>
<span data-ttu-id="9c49e-108">Cmdleten **Get-AzPrivateDnsZoneGroup** får en eller flera privata DNS-zonfiler.</span><span class="sxs-lookup"><span data-stu-id="9c49e-108">The **Get-AzPrivateDnsZoneGroup** cmdlet gets one or more private DNS zone groups.</span></span>

## <span data-ttu-id="9c49e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9c49e-109">EXAMPLES</span></span>

### <span data-ttu-id="9c49e-110">Exempel 1: Hämta gruppen privata DNS-zoner</span><span class="sxs-lookup"><span data-stu-id="9c49e-110">Example 1: Retrieve private DNS zone group</span></span>
```powershell
PS C:\> Get-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name "dnsgroup1"
Name                  : dnsgroup1
Id                    : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateEndpoints/test-pr-endpoint/privateDnsZoneGroups/dnsgroup1
ProvisioningState     : Succeeded
PrivateDnsZoneConfigs : [
                          {
                            "Name": "test-vault-azure-com",
                            "PrivateDnsZoneId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateDnsZones/test.vault.azure.com",
                            "RecordSets": []
                          }
                        ]
```

<span data-ttu-id="9c49e-111">Ovan exemplet får du en privat DNS-zonfil som heter dnsgroup1 i RG resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="9c49e-111">Above example gets a private DNS zone group named dnsgroup1 in the resource group rg.</span></span>

## <span data-ttu-id="9c49e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9c49e-112">PARAMETERS</span></span>

### <span data-ttu-id="9c49e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c49e-113">-DefaultProfile</span></span>
<span data-ttu-id="9c49e-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9c49e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c49e-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="9c49e-115">-Name</span></span>
<span data-ttu-id="9c49e-116">Namnet på den privata DNS-zonfilen.</span><span class="sxs-lookup"><span data-stu-id="9c49e-116">The name of the private dns zone group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases: PrivateDnsZoneGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c49e-117">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="9c49e-117">-PrivateEndpointName</span></span>
<span data-ttu-id="9c49e-118">Namnet på den privata slut punkten.</span><span class="sxs-lookup"><span data-stu-id="9c49e-118">The name of the private endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c49e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c49e-119">-ResourceGroupName</span></span>
<span data-ttu-id="9c49e-120">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9c49e-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c49e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c49e-121">CommonParameters</span></span>
<span data-ttu-id="9c49e-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c49e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c49e-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c49e-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c49e-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9c49e-124">INPUTS</span></span>

### <span data-ttu-id="9c49e-125">System. String</span><span class="sxs-lookup"><span data-stu-id="9c49e-125">System.String</span></span>

## <span data-ttu-id="9c49e-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9c49e-126">OUTPUTS</span></span>

### <span data-ttu-id="9c49e-127">Microsoft. Azure. commands. Networks. Models. PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="9c49e-127">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="9c49e-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9c49e-128">NOTES</span></span>

## <span data-ttu-id="9c49e-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9c49e-129">RELATED LINKS</span></span>
