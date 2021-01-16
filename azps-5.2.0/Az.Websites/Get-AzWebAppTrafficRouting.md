---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppTrafficRouting.md
ms.openlocfilehash: fb8d23ad24f8e9ab0b6e951d39ba7445d336176f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414843"
---
# <span data-ttu-id="9e6b1-101">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="9e6b1-101">Get-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="9e6b1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9e6b1-102">SYNOPSIS</span></span>
<span data-ttu-id="9e6b1-103">Skaffa en routningsregler för det angivna plats namnet.</span><span class="sxs-lookup"><span data-stu-id="9e6b1-103">Get a routing Rule for the given Slot name.</span></span>

## <span data-ttu-id="9e6b1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9e6b1-104">SYNTAX</span></span>

```
Get-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RuleName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e6b1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9e6b1-105">DESCRIPTION</span></span>
<span data-ttu-id="9e6b1-106">Cmdleten **Get-AzWebAppTrafficRouting** hämtar en regel konfiguration för routning från en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="9e6b1-106">The **Get-AzWebAppTrafficRouting** cmdlet Gets a routing rule configuration from an Azure Web App Slot.</span></span>

## <span data-ttu-id="9e6b1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9e6b1-107">EXAMPLES</span></span>

### <span data-ttu-id="9e6b1-108">Exempel 1 hämtar regeln för specifik routning från webapp-facket</span><span class="sxs-lookup"><span data-stu-id="9e6b1-108">Example 1 Gets the specific routing rule from webapp slot</span></span>
```powershell
PS C:\> Get-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite"  -RuleName 'Stg'
```

<span data-ttu-id="9e6b1-109">Det här kommandot får en routningsregler för en viss webapp-plats.</span><span class="sxs-lookup"><span data-stu-id="9e6b1-109">This command gets a routing rule for a given webapp slot.</span></span>

## <span data-ttu-id="9e6b1-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9e6b1-110">PARAMETERS</span></span>

### <span data-ttu-id="9e6b1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e6b1-111">-DefaultProfile</span></span>
<span data-ttu-id="9e6b1-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9e6b1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e6b1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e6b1-113">-ResourceGroupName</span></span>
<span data-ttu-id="9e6b1-114">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="9e6b1-114">Resource Group Name</span></span>

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

### <span data-ttu-id="9e6b1-115">-RuleName</span><span class="sxs-lookup"><span data-stu-id="9e6b1-115">-RuleName</span></span>
<span data-ttu-id="9e6b1-116">Regel namn</span><span class="sxs-lookup"><span data-stu-id="9e6b1-116">Rule Name</span></span>
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

### <span data-ttu-id="9e6b1-117">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="9e6b1-117">-WebAppName</span></span>
<span data-ttu-id="9e6b1-118">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="9e6b1-118">WebApp Name</span></span>

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

### <span data-ttu-id="9e6b1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e6b1-119">CommonParameters</span></span>
<span data-ttu-id="9e6b1-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e6b1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e6b1-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e6b1-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e6b1-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9e6b1-122">INPUTS</span></span>

### <span data-ttu-id="9e6b1-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="9e6b1-123">None</span></span>

## <span data-ttu-id="9e6b1-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9e6b1-124">OUTPUTS</span></span>

### <span data-ttu-id="9e6b1-125">Microsoft. Azure. Management. webbplatser. Models. RampUpRule</span><span class="sxs-lookup"><span data-stu-id="9e6b1-125">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="9e6b1-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9e6b1-126">NOTES</span></span>

## <span data-ttu-id="9e6b1-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9e6b1-127">RELATED LINKS</span></span>

[<span data-ttu-id="9e6b1-128">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="9e6b1-128">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)

[<span data-ttu-id="9e6b1-129">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="9e6b1-129">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="9e6b1-130">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="9e6b1-130">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)
