---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/reset-Azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
ms.openlocfilehash: 519a072a0c51f489a78992e483dec8aa9cd1fab5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923293"
---
# <span data-ttu-id="95d23-101">Reset-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="95d23-101">Reset-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="95d23-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="95d23-102">SYNOPSIS</span></span>

## <span data-ttu-id="95d23-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="95d23-103">SYNTAX</span></span>

### <span data-ttu-id="95d23-104">S</span><span class="sxs-lookup"><span data-stu-id="95d23-104">S1</span></span>
```
Reset-AzWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95d23-105">S2</span><span class="sxs-lookup"><span data-stu-id="95d23-105">S2</span></span>
```
Reset-AzWebAppPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="95d23-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="95d23-106">DESCRIPTION</span></span>
<span data-ttu-id="95d23-107">Cmdleten **Reset-AzWebAppPublishingProfile** återställer publicerings profilen för det angivna webb programmet.</span><span class="sxs-lookup"><span data-stu-id="95d23-107">The **Reset-AzWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="95d23-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="95d23-108">EXAMPLES</span></span>

### <span data-ttu-id="95d23-109">9.1</span><span class="sxs-lookup"><span data-stu-id="95d23-109">1:</span></span>
```
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="95d23-110">Det här kommandot återställer publicerings profilen för Web App-ContosoWebApp som är kopplad till resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="95d23-110">This command resets the publishing profile for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="95d23-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="95d23-111">PARAMETERS</span></span>

### <span data-ttu-id="95d23-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95d23-112">-DefaultProfile</span></span>
<span data-ttu-id="95d23-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="95d23-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95d23-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="95d23-114">-Name</span></span>
<span data-ttu-id="95d23-115">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="95d23-115">WebApp Name</span></span>

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

### <span data-ttu-id="95d23-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95d23-116">-ResourceGroupName</span></span>
<span data-ttu-id="95d23-117">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="95d23-117">Resource Group Name</span></span>

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

### <span data-ttu-id="95d23-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="95d23-118">-WebApp</span></span>
<span data-ttu-id="95d23-119">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="95d23-119">WebApp Object</span></span>

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

### <span data-ttu-id="95d23-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95d23-120">CommonParameters</span></span>
<span data-ttu-id="95d23-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95d23-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95d23-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95d23-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95d23-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="95d23-123">INPUTS</span></span>

### <span data-ttu-id="95d23-124">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="95d23-124">Site</span></span>
<span data-ttu-id="95d23-125">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="95d23-125">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="95d23-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="95d23-126">OUTPUTS</span></span>

## <span data-ttu-id="95d23-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="95d23-127">NOTES</span></span>

## <span data-ttu-id="95d23-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="95d23-128">RELATED LINKS</span></span>

