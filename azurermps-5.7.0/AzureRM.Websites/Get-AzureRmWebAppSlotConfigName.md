---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotConfigName.md
ms.openlocfilehash: 96e9c5945938addfbd629ef66b5f68e54c0427e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575419"
---
# <span data-ttu-id="98569-101">Get-AzureRmWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="98569-101">Get-AzureRmWebAppSlotConfigName</span></span>

## <span data-ttu-id="98569-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="98569-102">SYNOPSIS</span></span>
<span data-ttu-id="98569-103">Hämta listan med webb program plats konfigurations namn</span><span class="sxs-lookup"><span data-stu-id="98569-103">Get the list of Web App Slot Config names</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98569-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="98569-104">SYNTAX</span></span>

### <span data-ttu-id="98569-105">S</span><span class="sxs-lookup"><span data-stu-id="98569-105">S1</span></span>
```
Get-AzureRmWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98569-106">S2</span><span class="sxs-lookup"><span data-stu-id="98569-106">S2</span></span>
```
Get-AzureRmWebAppSlotConfigName [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="98569-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="98569-107">DESCRIPTION</span></span>
<span data-ttu-id="98569-108">Cmdleten **Get-AzureRmWebAppSlotConfigName** hämtar listan över program inställningar och anslutnings Strängs namn som för närvarande är markerade som plats inställningar</span><span class="sxs-lookup"><span data-stu-id="98569-108">The **Get-AzureRmWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="98569-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="98569-109">EXAMPLES</span></span>

### <span data-ttu-id="98569-110">9.1</span><span class="sxs-lookup"><span data-stu-id="98569-110">1:</span></span>
```
PS C:\>Get-AzureRmWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="98569-111">Det här kommandot får program inställningar och anslutnings strängar som hör till webb programmet som heter ContosoSite associerat med resurs gruppens standard-väst</span><span class="sxs-lookup"><span data-stu-id="98569-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="98569-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="98569-112">PARAMETERS</span></span>

### <span data-ttu-id="98569-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98569-113">-DefaultProfile</span></span>
<span data-ttu-id="98569-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="98569-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98569-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="98569-115">-Name</span></span>
<span data-ttu-id="98569-116">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="98569-116">WebApp Name</span></span>

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

### <span data-ttu-id="98569-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98569-117">-ResourceGroupName</span></span>
<span data-ttu-id="98569-118">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="98569-118">Resource Group Name</span></span>

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

### <span data-ttu-id="98569-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="98569-119">-WebApp</span></span>
<span data-ttu-id="98569-120">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="98569-120">WebApp Object</span></span>

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

### <span data-ttu-id="98569-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98569-121">CommonParameters</span></span>
<span data-ttu-id="98569-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98569-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98569-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98569-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98569-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="98569-124">INPUTS</span></span>

### <span data-ttu-id="98569-125">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="98569-125">Site</span></span>
<span data-ttu-id="98569-126">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="98569-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="98569-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="98569-127">OUTPUTS</span></span>

## <span data-ttu-id="98569-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="98569-128">NOTES</span></span>

## <span data-ttu-id="98569-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="98569-129">RELATED LINKS</span></span>

