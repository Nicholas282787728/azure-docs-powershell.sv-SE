---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotConfigName.md
ms.openlocfilehash: b1b9760d129a4177f979996f1ef46bd2a225f452
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755180"
---
# <span data-ttu-id="d3218-101">Get-AzureRmWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="d3218-101">Get-AzureRmWebAppSlotConfigName</span></span>

## <span data-ttu-id="d3218-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d3218-102">SYNOPSIS</span></span>
<span data-ttu-id="d3218-103">Hämta listan med webb program plats konfigurations namn</span><span class="sxs-lookup"><span data-stu-id="d3218-103">Get the list of Web App Slot Config names</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3218-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d3218-104">SYNTAX</span></span>

### <span data-ttu-id="d3218-105">S</span><span class="sxs-lookup"><span data-stu-id="d3218-105">S1</span></span>
```
Get-AzureRmWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3218-106">S2</span><span class="sxs-lookup"><span data-stu-id="d3218-106">S2</span></span>
```
Get-AzureRmWebAppSlotConfigName [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d3218-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d3218-107">DESCRIPTION</span></span>
<span data-ttu-id="d3218-108">Cmdleten **Get-AzureRmWebAppSlotConfigName** hämtar listan över program inställningar och anslutnings Strängs namn som för närvarande är markerade som plats inställningar</span><span class="sxs-lookup"><span data-stu-id="d3218-108">The **Get-AzureRmWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="d3218-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d3218-109">EXAMPLES</span></span>

### <span data-ttu-id="d3218-110">9.1</span><span class="sxs-lookup"><span data-stu-id="d3218-110">1:</span></span>
```
PS C:\>Get-AzureRmWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="d3218-111">Det här kommandot får program inställningar och anslutnings strängar som hör till webb programmet som heter ContosoSite associerat med resurs gruppens standard-väst</span><span class="sxs-lookup"><span data-stu-id="d3218-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="d3218-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d3218-112">PARAMETERS</span></span>

### <span data-ttu-id="d3218-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3218-113">-DefaultProfile</span></span>
<span data-ttu-id="d3218-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d3218-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3218-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="d3218-115">-Name</span></span>
<span data-ttu-id="d3218-116">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="d3218-116">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3218-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3218-117">-ResourceGroupName</span></span>
<span data-ttu-id="d3218-118">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="d3218-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3218-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d3218-119">-WebApp</span></span>
<span data-ttu-id="d3218-120">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="d3218-120">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3218-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3218-121">CommonParameters</span></span>
<span data-ttu-id="d3218-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3218-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3218-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3218-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3218-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d3218-124">INPUTS</span></span>

### <span data-ttu-id="d3218-125">System. String</span><span class="sxs-lookup"><span data-stu-id="d3218-125">System.String</span></span>

### <span data-ttu-id="d3218-126">Microsoft. Azure. Management. webbplatser. Models. site</span><span class="sxs-lookup"><span data-stu-id="d3218-126">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="d3218-127">Parametrar: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d3218-127">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="d3218-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d3218-128">OUTPUTS</span></span>

### <span data-ttu-id="d3218-129">Microsoft. Azure. Management. webbplatser. Models. SlotConfigNamesResource</span><span class="sxs-lookup"><span data-stu-id="d3218-129">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="d3218-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d3218-130">NOTES</span></span>

## <span data-ttu-id="d3218-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d3218-131">RELATED LINKS</span></span>
