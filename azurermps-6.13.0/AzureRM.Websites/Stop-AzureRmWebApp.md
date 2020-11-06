---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/stop-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebApp.md
ms.openlocfilehash: b389a84ea57902e2e7a7dabaea2d853827a728e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573816"
---
# <span data-ttu-id="e8bbf-101">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="e8bbf-101">Stop-AzureRmWebApp</span></span>

## <span data-ttu-id="e8bbf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e8bbf-102">SYNOPSIS</span></span>
<span data-ttu-id="e8bbf-103">Stoppar en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="e8bbf-103">Stops an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8bbf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e8bbf-104">SYNTAX</span></span>

### <span data-ttu-id="e8bbf-105">S</span><span class="sxs-lookup"><span data-stu-id="e8bbf-105">S1</span></span>
```
Stop-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e8bbf-106">S2</span><span class="sxs-lookup"><span data-stu-id="e8bbf-106">S2</span></span>
```
Stop-AzureRmWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8bbf-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e8bbf-107">DESCRIPTION</span></span>
<span data-ttu-id="e8bbf-108">Cmdleten **Stop-AzureRmWebApp** stoppar en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="e8bbf-108">The **Stop-AzureRmWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="e8bbf-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e8bbf-109">EXAMPLES</span></span>

### <span data-ttu-id="e8bbf-110">Exempel 1: stoppa ett webb program</span><span class="sxs-lookup"><span data-stu-id="e8bbf-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="e8bbf-111">Det här kommandot stoppar webb programmet som heter ContosoWebApp som tillhör resurs gruppen som heter default-West-väst.</span><span class="sxs-lookup"><span data-stu-id="e8bbf-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="e8bbf-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e8bbf-112">PARAMETERS</span></span>

### <span data-ttu-id="e8bbf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8bbf-113">-DefaultProfile</span></span>
<span data-ttu-id="e8bbf-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e8bbf-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8bbf-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="e8bbf-115">-Name</span></span>
<span data-ttu-id="e8bbf-116">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="e8bbf-116">WebApp Name</span></span>

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

### <span data-ttu-id="e8bbf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8bbf-117">-ResourceGroupName</span></span>
<span data-ttu-id="e8bbf-118">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="e8bbf-118">Resource Group Name</span></span>

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

### <span data-ttu-id="e8bbf-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="e8bbf-119">-WebApp</span></span>
<span data-ttu-id="e8bbf-120">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="e8bbf-120">WebApp Object</span></span>

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

### <span data-ttu-id="e8bbf-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8bbf-121">CommonParameters</span></span>
<span data-ttu-id="e8bbf-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8bbf-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8bbf-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8bbf-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8bbf-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e8bbf-124">INPUTS</span></span>

### <span data-ttu-id="e8bbf-125">System. String</span><span class="sxs-lookup"><span data-stu-id="e8bbf-125">System.String</span></span>

### <span data-ttu-id="e8bbf-126">Microsoft. Azure. Management. webbplatser. Models. site</span><span class="sxs-lookup"><span data-stu-id="e8bbf-126">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="e8bbf-127">Parametrar: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e8bbf-127">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="e8bbf-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e8bbf-128">OUTPUTS</span></span>

### <span data-ttu-id="e8bbf-129">Microsoft. Azure. Management. webbplatser. Models. site</span><span class="sxs-lookup"><span data-stu-id="e8bbf-129">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="e8bbf-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e8bbf-130">NOTES</span></span>

## <span data-ttu-id="e8bbf-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e8bbf-131">RELATED LINKS</span></span>

[<span data-ttu-id="e8bbf-132">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="e8bbf-132">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="e8bbf-133">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="e8bbf-133">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="e8bbf-134">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="e8bbf-134">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="e8bbf-135">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="e8bbf-135">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="e8bbf-136">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="e8bbf-136">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)


