---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/reset-azurermwebapppublishingprofile
schema: 2.0.0
ms.openlocfilehash: f082241be9e31b11782fcbbf5570a7f3c3947012
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928630"
---
# <span data-ttu-id="7f0aa-101">Reset-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="7f0aa-101">Reset-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="7f0aa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7f0aa-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f0aa-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7f0aa-103">SYNTAX</span></span>

### <span data-ttu-id="7f0aa-104">S</span><span class="sxs-lookup"><span data-stu-id="7f0aa-104">S1</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f0aa-105">S2</span><span class="sxs-lookup"><span data-stu-id="7f0aa-105">S2</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7f0aa-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7f0aa-106">DESCRIPTION</span></span>
<span data-ttu-id="7f0aa-107">Cmdleten **Reset-AzureRmWebAppPublishingProfile** återställer publicerings profilen för det angivna webb programmet.</span><span class="sxs-lookup"><span data-stu-id="7f0aa-107">The **Reset-AzureRmWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="7f0aa-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7f0aa-108">EXAMPLES</span></span>

### <span data-ttu-id="7f0aa-109">9.1</span><span class="sxs-lookup"><span data-stu-id="7f0aa-109">1:</span></span>
```
PS C:\> Reset-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="7f0aa-110">Det här kommandot återställer publicerings profilen för Web App-ContosoWebApp som är kopplad till resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="7f0aa-110">This command resets the publishing profile for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="7f0aa-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7f0aa-111">PARAMETERS</span></span>

### <span data-ttu-id="7f0aa-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f0aa-112">-DefaultProfile</span></span>
<span data-ttu-id="7f0aa-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7f0aa-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f0aa-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="7f0aa-114">-Name</span></span>
<span data-ttu-id="7f0aa-115">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="7f0aa-115">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f0aa-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f0aa-116">-ResourceGroupName</span></span>
<span data-ttu-id="7f0aa-117">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="7f0aa-117">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f0aa-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="7f0aa-118">-WebApp</span></span>
<span data-ttu-id="7f0aa-119">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="7f0aa-119">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f0aa-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f0aa-120">CommonParameters</span></span>
<span data-ttu-id="7f0aa-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f0aa-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f0aa-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f0aa-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f0aa-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7f0aa-123">INPUTS</span></span>

### <span data-ttu-id="7f0aa-124">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="7f0aa-124">Site</span></span>
<span data-ttu-id="7f0aa-125">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="7f0aa-125">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="7f0aa-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7f0aa-126">OUTPUTS</span></span>

## <span data-ttu-id="7f0aa-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7f0aa-127">NOTES</span></span>

## <span data-ttu-id="7f0aa-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7f0aa-128">RELATED LINKS</span></span>

