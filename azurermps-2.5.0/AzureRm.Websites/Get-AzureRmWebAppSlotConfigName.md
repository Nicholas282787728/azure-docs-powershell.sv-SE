---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslotconfigname
schema: 2.0.0
ms.openlocfilehash: ff05a30c495475b63b0385f3398c78e0b018a4bc
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930462"
---
# <span data-ttu-id="7328f-101">Get-AzureRmWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="7328f-101">Get-AzureRmWebAppSlotConfigName</span></span>

## <span data-ttu-id="7328f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7328f-102">SYNOPSIS</span></span>
<span data-ttu-id="7328f-103">Hämta listan med webb program plats konfigurations namn</span><span class="sxs-lookup"><span data-stu-id="7328f-103">Get the list of Web App Slot Config names</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7328f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7328f-104">SYNTAX</span></span>

### <span data-ttu-id="7328f-105">S</span><span class="sxs-lookup"><span data-stu-id="7328f-105">S1</span></span>
```
Get-AzureRmWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7328f-106">S2</span><span class="sxs-lookup"><span data-stu-id="7328f-106">S2</span></span>
```
Get-AzureRmWebAppSlotConfigName [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7328f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7328f-107">DESCRIPTION</span></span>
<span data-ttu-id="7328f-108">Cmdleten **Get-AzureRmWebAppSlotConfigName** hämtar listan över program inställningar och anslutnings Strängs namn som för närvarande är markerade som plats inställningar</span><span class="sxs-lookup"><span data-stu-id="7328f-108">The **Get-AzureRmWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="7328f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7328f-109">EXAMPLES</span></span>

### <span data-ttu-id="7328f-110">9.1</span><span class="sxs-lookup"><span data-stu-id="7328f-110">1:</span></span>
```
PS C:\>Get-AzureRmWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="7328f-111">Det här kommandot får program inställningar och anslutnings strängar som hör till webb programmet som heter ContosoSite associerat med resurs gruppens standard-väst</span><span class="sxs-lookup"><span data-stu-id="7328f-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="7328f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7328f-112">PARAMETERS</span></span>

### <span data-ttu-id="7328f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7328f-113">-DefaultProfile</span></span>
<span data-ttu-id="7328f-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7328f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7328f-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="7328f-115">-Name</span></span>
<span data-ttu-id="7328f-116">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="7328f-116">WebApp Name</span></span>

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

### <span data-ttu-id="7328f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7328f-117">-ResourceGroupName</span></span>
<span data-ttu-id="7328f-118">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="7328f-118">Resource Group Name</span></span>

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

### <span data-ttu-id="7328f-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="7328f-119">-WebApp</span></span>
<span data-ttu-id="7328f-120">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="7328f-120">WebApp Object</span></span>

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

### <span data-ttu-id="7328f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7328f-121">CommonParameters</span></span>
<span data-ttu-id="7328f-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7328f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7328f-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7328f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7328f-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7328f-124">INPUTS</span></span>

### <span data-ttu-id="7328f-125">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="7328f-125">Site</span></span>
<span data-ttu-id="7328f-126">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="7328f-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="7328f-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7328f-127">OUTPUTS</span></span>

## <span data-ttu-id="7328f-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7328f-128">NOTES</span></span>

## <span data-ttu-id="7328f-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7328f-129">RELATED LINKS</span></span>

