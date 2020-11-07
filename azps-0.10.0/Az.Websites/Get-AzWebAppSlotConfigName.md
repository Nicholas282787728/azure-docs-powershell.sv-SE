---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
ms.openlocfilehash: 414e25840b03127bbe94586248641e103c1f7d88
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923342"
---
# <span data-ttu-id="590df-101">Get-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="590df-101">Get-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="590df-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="590df-102">SYNOPSIS</span></span>
<span data-ttu-id="590df-103">Hämta listan med webb program plats konfigurations namn</span><span class="sxs-lookup"><span data-stu-id="590df-103">Get the list of Web App Slot Config names</span></span>

## <span data-ttu-id="590df-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="590df-104">SYNTAX</span></span>

### <span data-ttu-id="590df-105">S</span><span class="sxs-lookup"><span data-stu-id="590df-105">S1</span></span>
```
Get-AzWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="590df-106">S2</span><span class="sxs-lookup"><span data-stu-id="590df-106">S2</span></span>
```
Get-AzWebAppSlotConfigName [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="590df-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="590df-107">DESCRIPTION</span></span>
<span data-ttu-id="590df-108">Cmdleten **Get-AzWebAppSlotConfigName** hämtar listan över program inställningar och anslutnings Strängs namn som för närvarande är markerade som plats inställningar</span><span class="sxs-lookup"><span data-stu-id="590df-108">The **Get-AzWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="590df-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="590df-109">EXAMPLES</span></span>

### <span data-ttu-id="590df-110">9.1</span><span class="sxs-lookup"><span data-stu-id="590df-110">1:</span></span>
```
PS C:\>Get-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="590df-111">Det här kommandot får program inställningar och anslutnings strängar som hör till webb programmet som heter ContosoSite associerat med resurs gruppens standard-väst</span><span class="sxs-lookup"><span data-stu-id="590df-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="590df-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="590df-112">PARAMETERS</span></span>

### <span data-ttu-id="590df-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="590df-113">-DefaultProfile</span></span>
<span data-ttu-id="590df-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="590df-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="590df-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="590df-115">-Name</span></span>
<span data-ttu-id="590df-116">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="590df-116">WebApp Name</span></span>

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

### <span data-ttu-id="590df-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="590df-117">-ResourceGroupName</span></span>
<span data-ttu-id="590df-118">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="590df-118">Resource Group Name</span></span>

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

### <span data-ttu-id="590df-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="590df-119">-WebApp</span></span>
<span data-ttu-id="590df-120">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="590df-120">WebApp Object</span></span>

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

### <span data-ttu-id="590df-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="590df-121">CommonParameters</span></span>
<span data-ttu-id="590df-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="590df-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="590df-123">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="590df-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="590df-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="590df-124">INPUTS</span></span>

### <span data-ttu-id="590df-125">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="590df-125">Site</span></span>
<span data-ttu-id="590df-126">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="590df-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="590df-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="590df-127">OUTPUTS</span></span>

## <span data-ttu-id="590df-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="590df-128">NOTES</span></span>

## <span data-ttu-id="590df-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="590df-129">RELATED LINKS</span></span>

