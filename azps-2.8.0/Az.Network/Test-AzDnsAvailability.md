---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 556A9F12-DF72-468F-9C3F-A747CC70BD2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azdnsavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
ms.openlocfilehash: 6d6626164000957ffaa987a71131987f35a977c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919438"
---
# <span data-ttu-id="cadad-101">Test-AzDnsAvailability</span><span class="sxs-lookup"><span data-stu-id="cadad-101">Test-AzDnsAvailability</span></span>

## <span data-ttu-id="cadad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cadad-102">SYNOPSIS</span></span>
<span data-ttu-id="cadad-103">Kontrollerar om ett domän namn i cloudapp.azure.com-zonen är tillgängligt för användning.</span><span class="sxs-lookup"><span data-stu-id="cadad-103">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="cadad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cadad-104">SYNTAX</span></span>

```
Test-AzDnsAvailability -DomainNameLabel <String> -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cadad-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cadad-105">DESCRIPTION</span></span>
<span data-ttu-id="cadad-106">Kontrollerar om ett domän namn i cloudapp.azure.com-zonen är tillgängligt för användning.</span><span class="sxs-lookup"><span data-stu-id="cadad-106">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="cadad-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cadad-107">EXAMPLES</span></span>

### <span data-ttu-id="cadad-108">Exempel 1: kontrol lera om contoso.cloudapp.azure.com är tillgängligt för användning.</span><span class="sxs-lookup"><span data-stu-id="cadad-108">Example 1: Check if contoso.cloudapp.azure.com is available for use.</span></span>
```
Test-AzDnsAvailability -DomainNameLabel contoso -Location westus
```

## <span data-ttu-id="cadad-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cadad-109">PARAMETERS</span></span>

### <span data-ttu-id="cadad-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cadad-110">-DefaultProfile</span></span>
<span data-ttu-id="cadad-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cadad-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cadad-112">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="cadad-112">-DomainNameLabel</span></span>
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

### <span data-ttu-id="cadad-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="cadad-113">-Location</span></span>
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

### <span data-ttu-id="cadad-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cadad-114">CommonParameters</span></span>
<span data-ttu-id="cadad-115">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cadad-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cadad-116">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cadad-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cadad-117">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cadad-117">INPUTS</span></span>

### <span data-ttu-id="cadad-118">Ingen</span><span class="sxs-lookup"><span data-stu-id="cadad-118">None</span></span>

## <span data-ttu-id="cadad-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cadad-119">OUTPUTS</span></span>

### <span data-ttu-id="cadad-120">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cadad-120">System.Boolean</span></span>

## <span data-ttu-id="cadad-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cadad-121">NOTES</span></span>

## <span data-ttu-id="cadad-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cadad-122">RELATED LINKS</span></span>
