---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotConfigName.md
ms.openlocfilehash: 196e653447204b65c7f431e29fe76078a268dda1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757733"
---
# <span data-ttu-id="fadad-101">Get-AzureRmWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="fadad-101">Get-AzureRmWebAppSlotConfigName</span></span>

## <span data-ttu-id="fadad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fadad-102">SYNOPSIS</span></span>
<span data-ttu-id="fadad-103">Hämta listan med webb program plats konfigurations namn</span><span class="sxs-lookup"><span data-stu-id="fadad-103">Get the list of Web App Slot Config names</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fadad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fadad-104">SYNTAX</span></span>

### <span data-ttu-id="fadad-105">S</span><span class="sxs-lookup"><span data-stu-id="fadad-105">S1</span></span>
```
Get-AzureRmWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fadad-106">S2</span><span class="sxs-lookup"><span data-stu-id="fadad-106">S2</span></span>
```
Get-AzureRmWebAppSlotConfigName [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fadad-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fadad-107">DESCRIPTION</span></span>
<span data-ttu-id="fadad-108">Cmdleten **Get-AzureRmWebAppSlotConfigName** hämtar listan över program inställningar och anslutnings Strängs namn som för närvarande är markerade som plats inställningar</span><span class="sxs-lookup"><span data-stu-id="fadad-108">The **Get-AzureRmWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="fadad-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fadad-109">EXAMPLES</span></span>

### <span data-ttu-id="fadad-110">9.1</span><span class="sxs-lookup"><span data-stu-id="fadad-110">1:</span></span>
```
PS C:\>Get-AzureRmWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="fadad-111">Det här kommandot får program inställningar och anslutnings strängar som hör till webb programmet som heter ContosoSite associerat med resurs gruppens standard-väst</span><span class="sxs-lookup"><span data-stu-id="fadad-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="fadad-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fadad-112">PARAMETERS</span></span>

### <span data-ttu-id="fadad-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="fadad-113">-Name</span></span>
<span data-ttu-id="fadad-114">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="fadad-114">WebApp Name</span></span>

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

### <span data-ttu-id="fadad-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fadad-115">-ResourceGroupName</span></span>
<span data-ttu-id="fadad-116">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="fadad-116">Resource Group Name</span></span>

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

### <span data-ttu-id="fadad-117">-WebApp</span><span class="sxs-lookup"><span data-stu-id="fadad-117">-WebApp</span></span>
<span data-ttu-id="fadad-118">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="fadad-118">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fadad-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fadad-119">-DefaultProfile</span></span>
<span data-ttu-id="fadad-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fadad-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fadad-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fadad-121">CommonParameters</span></span>
<span data-ttu-id="fadad-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fadad-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fadad-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fadad-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fadad-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fadad-124">INPUTS</span></span>

### <span data-ttu-id="fadad-125">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="fadad-125">Site</span></span>
<span data-ttu-id="fadad-126">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="fadad-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="fadad-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fadad-127">OUTPUTS</span></span>

## <span data-ttu-id="fadad-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fadad-128">NOTES</span></span>

## <span data-ttu-id="fadad-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fadad-129">RELATED LINKS</span></span>

