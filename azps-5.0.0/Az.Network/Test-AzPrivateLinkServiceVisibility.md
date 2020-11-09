---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azprivatelinkservicevisibility
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
ms.openlocfilehash: f443928a8a616e8b8c6c13e5ae941aff607638ef
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325169"
---
# <span data-ttu-id="4b5d6-101">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="4b5d6-101">Test-AzPrivateLinkServiceVisibility</span></span>

## <span data-ttu-id="4b5d6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4b5d6-102">SYNOPSIS</span></span>
<span data-ttu-id="4b5d6-103">**Testet-AzPrivateLinkServiceVisibility** kontrollerar om en privat länk tjänst är synlig för aktuell användning.</span><span class="sxs-lookup"><span data-stu-id="4b5d6-103">The **Test-AzPrivateLinkServiceVisibility** checks whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="4b5d6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4b5d6-104">SYNTAX</span></span>

```
Test-AzPrivateLinkServiceVisibility -Location <String> [-ResourceGroupName <String>]
 -PrivateLinkServiceAlias <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b5d6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4b5d6-105">DESCRIPTION</span></span>
<span data-ttu-id="4b5d6-106">Kontrol lera om en privat länk tjänst är synlig för användning.</span><span class="sxs-lookup"><span data-stu-id="4b5d6-106">Check whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="4b5d6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4b5d6-107">EXAMPLES</span></span>

### <span data-ttu-id="4b5d6-108">Exempel 1: kontrol lera om contoso.cloudapp.azure.com är tillgängligt för användning.</span><span class="sxs-lookup"><span data-stu-id="4b5d6-108">Example 1: Check if contoso.cloudapp.azure.com is available for use.</span></span>
```
Test-AzPrivateLinkServiceVisibility -Location westus -PrivateLinkServiceAlias "TestPLS.00000000-0000-0000-0000-000000000000.azure.privatelinkservice"
```

## <span data-ttu-id="4b5d6-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4b5d6-109">PARAMETERS</span></span>

### <span data-ttu-id="4b5d6-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b5d6-110">-DefaultProfile</span></span>
<span data-ttu-id="4b5d6-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4b5d6-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b5d6-112">-Plats</span><span class="sxs-lookup"><span data-stu-id="4b5d6-112">-Location</span></span>
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

### <span data-ttu-id="4b5d6-113">-PrivateLinkServiceAlias</span><span class="sxs-lookup"><span data-stu-id="4b5d6-113">-PrivateLinkServiceAlias</span></span>
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

### <span data-ttu-id="4b5d6-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b5d6-114">-ResourceGroupName</span></span>
<span data-ttu-id="4b5d6-115">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4b5d6-115">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b5d6-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b5d6-116">CommonParameters</span></span>
<span data-ttu-id="4b5d6-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b5d6-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b5d6-118">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b5d6-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b5d6-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4b5d6-119">INPUTS</span></span>

### <span data-ttu-id="4b5d6-120">Ingen</span><span class="sxs-lookup"><span data-stu-id="4b5d6-120">None</span></span>

## <span data-ttu-id="4b5d6-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4b5d6-121">OUTPUTS</span></span>

### <span data-ttu-id="4b5d6-122">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4b5d6-122">System.Boolean</span></span>

## <span data-ttu-id="4b5d6-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4b5d6-123">NOTES</span></span>

## <span data-ttu-id="4b5d6-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4b5d6-124">RELATED LINKS</span></span>
