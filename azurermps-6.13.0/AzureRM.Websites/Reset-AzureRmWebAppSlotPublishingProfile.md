---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/reset-azurermwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppSlotPublishingProfile.md
ms.openlocfilehash: 948088f99e90af4594e239dc379133955340e1d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577744"
---
# <span data-ttu-id="2779e-101">Reset-AzureRmWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="2779e-101">Reset-AzureRmWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="2779e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2779e-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2779e-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2779e-103">SYNTAX</span></span>

### <span data-ttu-id="2779e-104">S</span><span class="sxs-lookup"><span data-stu-id="2779e-104">S1</span></span>
```
Reset-AzureRmWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2779e-105">S2</span><span class="sxs-lookup"><span data-stu-id="2779e-105">S2</span></span>
```
Reset-AzureRmWebAppSlotPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2779e-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2779e-106">DESCRIPTION</span></span>
<span data-ttu-id="2779e-107">Cmdleten **Reset-AzureRmWebAppSlotPublishingProfile** återställer publicerings profilen för den angivna Web App-platsen.</span><span class="sxs-lookup"><span data-stu-id="2779e-107">The **Reset-AzureRmWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="2779e-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2779e-108">EXAMPLES</span></span>

### <span data-ttu-id="2779e-109">9.1</span><span class="sxs-lookup"><span data-stu-id="2779e-109">1:</span></span>
```
PS C:\> Reset-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="2779e-110">Det här kommandot återställer publicerings profilen för den plats som heter slot001 för Web App-ContosoWebApp som är kopplad till resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="2779e-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="2779e-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2779e-111">PARAMETERS</span></span>

### <span data-ttu-id="2779e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2779e-112">-DefaultProfile</span></span>
<span data-ttu-id="2779e-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2779e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2779e-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="2779e-114">-Name</span></span>
<span data-ttu-id="2779e-115">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="2779e-115">WebApp Name</span></span>

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

### <span data-ttu-id="2779e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2779e-116">-ResourceGroupName</span></span>
<span data-ttu-id="2779e-117">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="2779e-117">Resource Group Name</span></span>

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

### <span data-ttu-id="2779e-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="2779e-118">-Slot</span></span>
<span data-ttu-id="2779e-119">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="2779e-119">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2779e-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="2779e-120">-WebApp</span></span>
<span data-ttu-id="2779e-121">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="2779e-121">WebApp Object</span></span>

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

### <span data-ttu-id="2779e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2779e-122">CommonParameters</span></span>
<span data-ttu-id="2779e-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2779e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2779e-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2779e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2779e-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2779e-125">INPUTS</span></span>

### <span data-ttu-id="2779e-126">System. String</span><span class="sxs-lookup"><span data-stu-id="2779e-126">System.String</span></span>

### <span data-ttu-id="2779e-127">Microsoft. Azure. Management. webbplatser. Models. site</span><span class="sxs-lookup"><span data-stu-id="2779e-127">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="2779e-128">Parametrar: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2779e-128">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="2779e-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2779e-129">OUTPUTS</span></span>

### <span data-ttu-id="2779e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2779e-130">System.String</span></span>

## <span data-ttu-id="2779e-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2779e-131">NOTES</span></span>

## <span data-ttu-id="2779e-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2779e-132">RELATED LINKS</span></span>
