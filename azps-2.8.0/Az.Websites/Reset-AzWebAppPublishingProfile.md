---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/reset-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
ms.openlocfilehash: 81eaa3b287a14cdc9aa71150c2f0b3724aeb4f4b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920814"
---
# <span data-ttu-id="0ffed-101">Reset-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="0ffed-101">Reset-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="0ffed-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0ffed-102">SYNOPSIS</span></span>

## <span data-ttu-id="0ffed-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0ffed-103">SYNTAX</span></span>

### <span data-ttu-id="0ffed-104">S</span><span class="sxs-lookup"><span data-stu-id="0ffed-104">S1</span></span>
```
Reset-AzWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ffed-105">S2</span><span class="sxs-lookup"><span data-stu-id="0ffed-105">S2</span></span>
```
Reset-AzWebAppPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0ffed-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0ffed-106">DESCRIPTION</span></span>
<span data-ttu-id="0ffed-107">Cmdleten **Reset-AzWebAppPublishingProfile** återställer publicerings profilen för det angivna webb programmet.</span><span class="sxs-lookup"><span data-stu-id="0ffed-107">The **Reset-AzWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="0ffed-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0ffed-108">EXAMPLES</span></span>

### <span data-ttu-id="0ffed-109">9.1</span><span class="sxs-lookup"><span data-stu-id="0ffed-109">1:</span></span>
```
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="0ffed-110">Det här kommandot återställer publicerings profilen för Web App-ContosoWebApp som är kopplad till resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="0ffed-110">This command resets the publishing profile for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="0ffed-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0ffed-111">PARAMETERS</span></span>

### <span data-ttu-id="0ffed-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ffed-112">-DefaultProfile</span></span>
<span data-ttu-id="0ffed-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0ffed-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ffed-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="0ffed-114">-Name</span></span>
<span data-ttu-id="0ffed-115">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="0ffed-115">WebApp Name</span></span>

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

### <span data-ttu-id="0ffed-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ffed-116">-ResourceGroupName</span></span>
<span data-ttu-id="0ffed-117">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="0ffed-117">Resource Group Name</span></span>

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

### <span data-ttu-id="0ffed-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="0ffed-118">-WebApp</span></span>
<span data-ttu-id="0ffed-119">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="0ffed-119">WebApp Object</span></span>

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

### <span data-ttu-id="0ffed-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ffed-120">CommonParameters</span></span>
<span data-ttu-id="0ffed-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ffed-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ffed-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ffed-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ffed-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0ffed-123">INPUTS</span></span>

### <span data-ttu-id="0ffed-124">System. String</span><span class="sxs-lookup"><span data-stu-id="0ffed-124">System.String</span></span>

### <span data-ttu-id="0ffed-125">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="0ffed-125">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="0ffed-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0ffed-126">OUTPUTS</span></span>

### <span data-ttu-id="0ffed-127">System. String</span><span class="sxs-lookup"><span data-stu-id="0ffed-127">System.String</span></span>

## <span data-ttu-id="0ffed-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0ffed-128">NOTES</span></span>

## <span data-ttu-id="0ffed-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0ffed-129">RELATED LINKS</span></span>
