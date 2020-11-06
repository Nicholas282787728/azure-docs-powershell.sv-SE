---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/reset-azurermwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppPublishingProfile.md
ms.openlocfilehash: 096b062325ddfa12eba1d8c0fe8d6a154c3e77fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577748"
---
# <span data-ttu-id="dba01-101">Reset-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="dba01-101">Reset-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="dba01-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dba01-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dba01-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dba01-103">SYNTAX</span></span>

### <span data-ttu-id="dba01-104">S</span><span class="sxs-lookup"><span data-stu-id="dba01-104">S1</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dba01-105">S2</span><span class="sxs-lookup"><span data-stu-id="dba01-105">S2</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dba01-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dba01-106">DESCRIPTION</span></span>
<span data-ttu-id="dba01-107">Cmdleten **Reset-AzureRmWebAppPublishingProfile** återställer publicerings profilen för det angivna webb programmet.</span><span class="sxs-lookup"><span data-stu-id="dba01-107">The **Reset-AzureRmWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="dba01-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dba01-108">EXAMPLES</span></span>

### <span data-ttu-id="dba01-109">9.1</span><span class="sxs-lookup"><span data-stu-id="dba01-109">1:</span></span>
```
PS C:\> Reset-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="dba01-110">Det här kommandot återställer publicerings profilen för Web App-ContosoWebApp som är kopplad till resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="dba01-110">This command resets the publishing profile for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="dba01-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dba01-111">PARAMETERS</span></span>

### <span data-ttu-id="dba01-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dba01-112">-DefaultProfile</span></span>
<span data-ttu-id="dba01-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dba01-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dba01-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="dba01-114">-Name</span></span>
<span data-ttu-id="dba01-115">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="dba01-115">WebApp Name</span></span>

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

### <span data-ttu-id="dba01-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dba01-116">-ResourceGroupName</span></span>
<span data-ttu-id="dba01-117">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="dba01-117">Resource Group Name</span></span>

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

### <span data-ttu-id="dba01-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="dba01-118">-WebApp</span></span>
<span data-ttu-id="dba01-119">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="dba01-119">WebApp Object</span></span>

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

### <span data-ttu-id="dba01-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dba01-120">CommonParameters</span></span>
<span data-ttu-id="dba01-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dba01-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dba01-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dba01-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dba01-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dba01-123">INPUTS</span></span>

### <span data-ttu-id="dba01-124">System. String</span><span class="sxs-lookup"><span data-stu-id="dba01-124">System.String</span></span>

### <span data-ttu-id="dba01-125">Microsoft. Azure. Management. webbplatser. Models. site</span><span class="sxs-lookup"><span data-stu-id="dba01-125">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="dba01-126">Parametrar: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="dba01-126">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="dba01-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dba01-127">OUTPUTS</span></span>

### <span data-ttu-id="dba01-128">System. String</span><span class="sxs-lookup"><span data-stu-id="dba01-128">System.String</span></span>

## <span data-ttu-id="dba01-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dba01-129">NOTES</span></span>

## <span data-ttu-id="dba01-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dba01-130">RELATED LINKS</span></span>
