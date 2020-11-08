---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 556A9F12-DF72-468F-9C3F-A747CC70BD2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azdnsavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
ms.openlocfilehash: 2ee468c47f22e90ce47b003dcae1becfb905134e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088829"
---
# <span data-ttu-id="526c6-101">Test-AzDnsAvailability</span><span class="sxs-lookup"><span data-stu-id="526c6-101">Test-AzDnsAvailability</span></span>

## <span data-ttu-id="526c6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="526c6-102">SYNOPSIS</span></span>
<span data-ttu-id="526c6-103">Kontrollerar om ett domän namn i cloudapp.azure.com-zonen är tillgängligt för användning.</span><span class="sxs-lookup"><span data-stu-id="526c6-103">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="526c6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="526c6-104">SYNTAX</span></span>

```
Test-AzDnsAvailability -DomainNameLabel <String> -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="526c6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="526c6-105">DESCRIPTION</span></span>
<span data-ttu-id="526c6-106">Kontrollerar om ett domän namn i cloudapp.azure.com-zonen är tillgängligt för användning.</span><span class="sxs-lookup"><span data-stu-id="526c6-106">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="526c6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="526c6-107">EXAMPLES</span></span>

### <span data-ttu-id="526c6-108">Exempel 1: kontrol lera om contoso.westus.cloudapp.azure.com är tillgängligt för användning.</span><span class="sxs-lookup"><span data-stu-id="526c6-108">Example 1: Check if contoso.westus.cloudapp.azure.com is available for use.</span></span>
```
Test-AzDnsAvailability -DomainNameLabel contoso -Location westus
```

## <span data-ttu-id="526c6-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="526c6-109">PARAMETERS</span></span>

### <span data-ttu-id="526c6-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="526c6-110">-DefaultProfile</span></span>
<span data-ttu-id="526c6-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="526c6-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="526c6-112">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="526c6-112">-DomainNameLabel</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainQualifiedName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="526c6-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="526c6-113">-Location</span></span>
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

### <span data-ttu-id="526c6-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="526c6-114">CommonParameters</span></span>
<span data-ttu-id="526c6-115">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="526c6-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="526c6-116">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="526c6-116">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="526c6-117">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="526c6-117">INPUTS</span></span>

### <span data-ttu-id="526c6-118">Ingen</span><span class="sxs-lookup"><span data-stu-id="526c6-118">None</span></span>

## <span data-ttu-id="526c6-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="526c6-119">OUTPUTS</span></span>

### <span data-ttu-id="526c6-120">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="526c6-120">System.Boolean</span></span>

## <span data-ttu-id="526c6-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="526c6-121">NOTES</span></span>

## <span data-ttu-id="526c6-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="526c6-122">RELATED LINKS</span></span>
