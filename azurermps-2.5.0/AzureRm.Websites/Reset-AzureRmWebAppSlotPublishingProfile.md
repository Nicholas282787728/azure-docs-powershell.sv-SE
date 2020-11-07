---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/reset-azurermwebappslotpublishingprofile
schema: 2.0.0
ms.openlocfilehash: 7c385f230456da60df76c56fc652dda53362c778
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931110"
---
# <span data-ttu-id="87eaf-101">Reset-AzureRmWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="87eaf-101">Reset-AzureRmWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="87eaf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="87eaf-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87eaf-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="87eaf-103">SYNTAX</span></span>

### <span data-ttu-id="87eaf-104">S</span><span class="sxs-lookup"><span data-stu-id="87eaf-104">S1</span></span>
```
Reset-AzureRmWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87eaf-105">S2</span><span class="sxs-lookup"><span data-stu-id="87eaf-105">S2</span></span>
```
Reset-AzureRmWebAppSlotPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="87eaf-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="87eaf-106">DESCRIPTION</span></span>
<span data-ttu-id="87eaf-107">Cmdleten **Reset-AzureRmWebAppSlotPublishingProfile** återställer publicerings profilen för den angivna Web App-platsen.</span><span class="sxs-lookup"><span data-stu-id="87eaf-107">The **Reset-AzureRmWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="87eaf-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="87eaf-108">EXAMPLES</span></span>

### <span data-ttu-id="87eaf-109">9.1</span><span class="sxs-lookup"><span data-stu-id="87eaf-109">1:</span></span>
```
PS C:\> Reset-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="87eaf-110">Det här kommandot återställer publicerings profilen för den plats som heter slot001 för Web App-ContosoWebApp som är kopplad till resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="87eaf-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="87eaf-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="87eaf-111">PARAMETERS</span></span>

### <span data-ttu-id="87eaf-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87eaf-112">-DefaultProfile</span></span>
<span data-ttu-id="87eaf-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="87eaf-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87eaf-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="87eaf-114">-Name</span></span>
<span data-ttu-id="87eaf-115">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="87eaf-115">WebApp Name</span></span>

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

### <span data-ttu-id="87eaf-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87eaf-116">-ResourceGroupName</span></span>
<span data-ttu-id="87eaf-117">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="87eaf-117">Resource Group Name</span></span>

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

### <span data-ttu-id="87eaf-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="87eaf-118">-Slot</span></span>
<span data-ttu-id="87eaf-119">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="87eaf-119">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87eaf-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="87eaf-120">-WebApp</span></span>
<span data-ttu-id="87eaf-121">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="87eaf-121">WebApp Object</span></span>

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

### <span data-ttu-id="87eaf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87eaf-122">CommonParameters</span></span>
<span data-ttu-id="87eaf-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87eaf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87eaf-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87eaf-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87eaf-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="87eaf-125">INPUTS</span></span>

### <span data-ttu-id="87eaf-126">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="87eaf-126">Site</span></span>
<span data-ttu-id="87eaf-127">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="87eaf-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="87eaf-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="87eaf-128">OUTPUTS</span></span>

## <span data-ttu-id="87eaf-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="87eaf-129">NOTES</span></span>

## <span data-ttu-id="87eaf-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="87eaf-130">RELATED LINKS</span></span>

