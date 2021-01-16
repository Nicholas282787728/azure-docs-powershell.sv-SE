---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableservicealias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceAlias.md
ms.openlocfilehash: acf9d604a793d4631641a87b222260d8687807cb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396531"
---
# <span data-ttu-id="703a6-101">Get-AzAvailableServiceAlias</span><span class="sxs-lookup"><span data-stu-id="703a6-101">Get-AzAvailableServiceAlias</span></span>

## <span data-ttu-id="703a6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="703a6-102">SYNOPSIS</span></span>
<span data-ttu-id="703a6-103">Få tillgängliga tjänst Ali Aset i regionen.</span><span class="sxs-lookup"><span data-stu-id="703a6-103">Get available service aliases in the region.</span></span>

## <span data-ttu-id="703a6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="703a6-104">SYNTAX</span></span>

```
Get-AzAvailableServiceAlias -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="703a6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="703a6-105">DESCRIPTION</span></span>
<span data-ttu-id="703a6-106">Med cmdleten **Get-AzAvailableServiceAlias** kan du hämta alla tillgängliga tjänst Ali Aset för ett undernät på den avsedda platsen.</span><span class="sxs-lookup"><span data-stu-id="703a6-106">The **Get-AzAvailableServiceAlias** cmdlet allows you to retrieve all of the available service aliases for a subnet in the provided location.</span></span>

## <span data-ttu-id="703a6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="703a6-107">EXAMPLES</span></span>

### <span data-ttu-id="703a6-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="703a6-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAvailableServiceAlias -Location "westus"

Name                         Id                                                                                                                                   Type                                      ResourceName
----                         --                                                                                                                                   ----                                      ------------
servicesAzure                /subscriptions/61dc4623-b5f8-41a0-acfc-29537dcf6e5d/providers/Microsoft.Network/AvailableServiceAliases/servicesAzure                Microsoft.Network/AvailableServiceAliases /services/Azure
servicesAzureManagedInstance /subscriptions/61dc4623-b5f8-41a0-acfc-29537dcf6e5d/providers/Microsoft.Network/AvailableServiceAliases/servicesAzureManagedInstance Microsoft.Network/AvailableServiceAliases /services/Azure/ManagedInstance

```

## <span data-ttu-id="703a6-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="703a6-109">PARAMETERS</span></span>

### <span data-ttu-id="703a6-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="703a6-110">-DefaultProfile</span></span>
<span data-ttu-id="703a6-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="703a6-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="703a6-112">-Plats</span><span class="sxs-lookup"><span data-stu-id="703a6-112">-Location</span></span>
<span data-ttu-id="703a6-113">Platsen.</span><span class="sxs-lookup"><span data-stu-id="703a6-113">The location.</span></span>

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

### <span data-ttu-id="703a6-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="703a6-114">CommonParameters</span></span>
<span data-ttu-id="703a6-115">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="703a6-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="703a6-116">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="703a6-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="703a6-117">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="703a6-117">INPUTS</span></span>

### <span data-ttu-id="703a6-118">System. String</span><span class="sxs-lookup"><span data-stu-id="703a6-118">System.String</span></span>

## <span data-ttu-id="703a6-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="703a6-119">OUTPUTS</span></span>

### <span data-ttu-id="703a6-120">Microsoft. Azure. commands. Networks. Models. PsAvailableServiceAlias</span><span class="sxs-lookup"><span data-stu-id="703a6-120">Microsoft.Azure.Commands.Network.Models.PsAvailableServiceAlias</span></span>

## <span data-ttu-id="703a6-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="703a6-121">NOTES</span></span>

## <span data-ttu-id="703a6-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="703a6-122">RELATED LINKS</span></span>
