---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/stop-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
ms.openlocfilehash: d08303ec0057a42569455c9e52c38e561de73e4d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262377"
---
# <span data-ttu-id="4c88a-101">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="4c88a-101">Stop-AzWebApp</span></span>

## <span data-ttu-id="4c88a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4c88a-102">SYNOPSIS</span></span>
<span data-ttu-id="4c88a-103">Stoppar en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="4c88a-103">Stops an Azure Web App.</span></span>

## <span data-ttu-id="4c88a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4c88a-104">SYNTAX</span></span>

### <span data-ttu-id="4c88a-105">S</span><span class="sxs-lookup"><span data-stu-id="4c88a-105">S1</span></span>
```
Stop-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4c88a-106">S2</span><span class="sxs-lookup"><span data-stu-id="4c88a-106">S2</span></span>
```
Stop-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c88a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4c88a-107">DESCRIPTION</span></span>
<span data-ttu-id="4c88a-108">Cmdleten **Stop-AzWebApp** stoppar en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="4c88a-108">The **Stop-AzWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="4c88a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4c88a-109">EXAMPLES</span></span>

### <span data-ttu-id="4c88a-110">Exempel 1: stoppa ett webb program</span><span class="sxs-lookup"><span data-stu-id="4c88a-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="4c88a-111">Det här kommandot stoppar webb programmet som heter ContosoWebApp som tillhör resurs gruppen som heter default-West-väst.</span><span class="sxs-lookup"><span data-stu-id="4c88a-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="4c88a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4c88a-112">PARAMETERS</span></span>

### <span data-ttu-id="4c88a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c88a-113">-DefaultProfile</span></span>
<span data-ttu-id="4c88a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4c88a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c88a-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="4c88a-115">-Name</span></span>
<span data-ttu-id="4c88a-116">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="4c88a-116">WebApp Name</span></span>

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

### <span data-ttu-id="4c88a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c88a-117">-ResourceGroupName</span></span>
<span data-ttu-id="4c88a-118">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="4c88a-118">Resource Group Name</span></span>

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

### <span data-ttu-id="4c88a-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="4c88a-119">-WebApp</span></span>
<span data-ttu-id="4c88a-120">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="4c88a-120">WebApp Object</span></span>

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

### <span data-ttu-id="4c88a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c88a-121">CommonParameters</span></span>
<span data-ttu-id="4c88a-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c88a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c88a-123">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c88a-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c88a-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4c88a-124">INPUTS</span></span>

### <span data-ttu-id="4c88a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="4c88a-125">System.String</span></span>

### <span data-ttu-id="4c88a-126">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="4c88a-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="4c88a-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4c88a-127">OUTPUTS</span></span>

### <span data-ttu-id="4c88a-128">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="4c88a-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="4c88a-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4c88a-129">NOTES</span></span>

## <span data-ttu-id="4c88a-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4c88a-130">RELATED LINKS</span></span>

[<span data-ttu-id="4c88a-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="4c88a-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="4c88a-132">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="4c88a-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="4c88a-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="4c88a-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="4c88a-134">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="4c88a-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="4c88a-135">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="4c88a-135">Start-AzWebApp</span></span>](./Start-AzWebApp.md)


