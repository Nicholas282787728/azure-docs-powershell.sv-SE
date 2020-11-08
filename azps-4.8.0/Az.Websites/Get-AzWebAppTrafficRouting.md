---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppTrafficRouting.md
ms.openlocfilehash: fb8d23ad24f8e9ab0b6e951d39ba7445d336176f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261158"
---
# <span data-ttu-id="b2977-101">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="b2977-101">Get-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="b2977-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b2977-102">SYNOPSIS</span></span>
<span data-ttu-id="b2977-103">Skaffa en routningsregler för det angivna plats namnet.</span><span class="sxs-lookup"><span data-stu-id="b2977-103">Get a routing Rule for the given Slot name.</span></span>

## <span data-ttu-id="b2977-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b2977-104">SYNTAX</span></span>

```
Get-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RuleName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2977-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b2977-105">DESCRIPTION</span></span>
<span data-ttu-id="b2977-106">Cmdleten **Get-AzWebAppTrafficRouting** hämtar en regel konfiguration för routning från en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="b2977-106">The **Get-AzWebAppTrafficRouting** cmdlet Gets a routing rule configuration from an Azure Web App Slot.</span></span>

## <span data-ttu-id="b2977-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b2977-107">EXAMPLES</span></span>

### <span data-ttu-id="b2977-108">Exempel 1 hämtar regeln för specifik routning från webapp-facket</span><span class="sxs-lookup"><span data-stu-id="b2977-108">Example 1 Gets the specific routing rule from webapp slot</span></span>
```powershell
PS C:\> Get-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite"  -RuleName 'Stg'
```

<span data-ttu-id="b2977-109">Det här kommandot får en routningsregler för en viss webapp-plats.</span><span class="sxs-lookup"><span data-stu-id="b2977-109">This command gets a routing rule for a given webapp slot.</span></span>

## <span data-ttu-id="b2977-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b2977-110">PARAMETERS</span></span>

### <span data-ttu-id="b2977-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2977-111">-DefaultProfile</span></span>
<span data-ttu-id="b2977-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b2977-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2977-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2977-113">-ResourceGroupName</span></span>
<span data-ttu-id="b2977-114">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="b2977-114">Resource Group Name</span></span>

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

### <span data-ttu-id="b2977-115">-RuleName</span><span class="sxs-lookup"><span data-stu-id="b2977-115">-RuleName</span></span>
<span data-ttu-id="b2977-116">Regel namn</span><span class="sxs-lookup"><span data-stu-id="b2977-116">Rule Name</span></span>
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

### <span data-ttu-id="b2977-117">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="b2977-117">-WebAppName</span></span>
<span data-ttu-id="b2977-118">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="b2977-118">WebApp Name</span></span>

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

### <span data-ttu-id="b2977-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2977-119">CommonParameters</span></span>
<span data-ttu-id="b2977-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2977-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2977-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2977-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2977-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b2977-122">INPUTS</span></span>

### <span data-ttu-id="b2977-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="b2977-123">None</span></span>

## <span data-ttu-id="b2977-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b2977-124">OUTPUTS</span></span>

### <span data-ttu-id="b2977-125">Microsoft. Azure. Management. webbplatser. Models. RampUpRule</span><span class="sxs-lookup"><span data-stu-id="b2977-125">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="b2977-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b2977-126">NOTES</span></span>

## <span data-ttu-id="b2977-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b2977-127">RELATED LINKS</span></span>

[<span data-ttu-id="b2977-128">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="b2977-128">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)

[<span data-ttu-id="b2977-129">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="b2977-129">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="b2977-130">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="b2977-130">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)
