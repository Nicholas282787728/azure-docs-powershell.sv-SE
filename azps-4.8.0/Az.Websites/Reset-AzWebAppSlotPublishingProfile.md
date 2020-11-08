---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/reset-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: 840e0bb2bfa10a89a5ba963e83ab434e795b3dd4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102524"
---
# <span data-ttu-id="afc9c-101">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="afc9c-101">Reset-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="afc9c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="afc9c-102">SYNOPSIS</span></span>

## <span data-ttu-id="afc9c-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="afc9c-103">SYNTAX</span></span>

### <span data-ttu-id="afc9c-104">S</span><span class="sxs-lookup"><span data-stu-id="afc9c-104">S1</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="afc9c-105">S2</span><span class="sxs-lookup"><span data-stu-id="afc9c-105">S2</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="afc9c-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="afc9c-106">DESCRIPTION</span></span>
<span data-ttu-id="afc9c-107">Cmdleten **Reset-AzWebAppSlotPublishingProfile** återställer publicerings profilen för den angivna Web App-platsen.</span><span class="sxs-lookup"><span data-stu-id="afc9c-107">The **Reset-AzWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="afc9c-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="afc9c-108">EXAMPLES</span></span>

### <span data-ttu-id="afc9c-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="afc9c-109">Example 1</span></span>
```powershell
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="afc9c-110">Det här kommandot återställer publicerings profilen för den plats som heter slot001 för Web App-ContosoWebApp som är kopplad till resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="afc9c-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="afc9c-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="afc9c-111">PARAMETERS</span></span>

### <span data-ttu-id="afc9c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afc9c-112">-DefaultProfile</span></span>
<span data-ttu-id="afc9c-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="afc9c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afc9c-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="afc9c-114">-Name</span></span>
<span data-ttu-id="afc9c-115">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="afc9c-115">WebApp Name</span></span>

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

### <span data-ttu-id="afc9c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afc9c-116">-ResourceGroupName</span></span>
<span data-ttu-id="afc9c-117">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="afc9c-117">Resource Group Name</span></span>

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

### <span data-ttu-id="afc9c-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="afc9c-118">-Slot</span></span>
<span data-ttu-id="afc9c-119">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="afc9c-119">WebApp Slot Name</span></span>

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

### <span data-ttu-id="afc9c-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="afc9c-120">-WebApp</span></span>
<span data-ttu-id="afc9c-121">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="afc9c-121">WebApp Object</span></span>

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

### <span data-ttu-id="afc9c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afc9c-122">CommonParameters</span></span>
<span data-ttu-id="afc9c-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afc9c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afc9c-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afc9c-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afc9c-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="afc9c-125">INPUTS</span></span>

### <span data-ttu-id="afc9c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="afc9c-126">System.String</span></span>

### <span data-ttu-id="afc9c-127">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="afc9c-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="afc9c-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="afc9c-128">OUTPUTS</span></span>

### <span data-ttu-id="afc9c-129">System. String</span><span class="sxs-lookup"><span data-stu-id="afc9c-129">System.String</span></span>

## <span data-ttu-id="afc9c-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="afc9c-130">NOTES</span></span>

## <span data-ttu-id="afc9c-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="afc9c-131">RELATED LINKS</span></span>
