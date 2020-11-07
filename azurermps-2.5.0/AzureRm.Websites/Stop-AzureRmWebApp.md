---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/stop-azurermwebapp
schema: 2.0.0
ms.openlocfilehash: 0e1c1b9a2aa20546db1306b47b54b18c2b0cd99e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930441"
---
# <span data-ttu-id="e32fb-101">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="e32fb-101">Stop-AzureRmWebApp</span></span>

## <span data-ttu-id="e32fb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e32fb-102">SYNOPSIS</span></span>
<span data-ttu-id="e32fb-103">Stoppar en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="e32fb-103">Stops an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e32fb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e32fb-104">SYNTAX</span></span>

### <span data-ttu-id="e32fb-105">S</span><span class="sxs-lookup"><span data-stu-id="e32fb-105">S1</span></span>
```
Stop-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e32fb-106">S2</span><span class="sxs-lookup"><span data-stu-id="e32fb-106">S2</span></span>
```
Stop-AzureRmWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e32fb-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e32fb-107">DESCRIPTION</span></span>
<span data-ttu-id="e32fb-108">Cmdleten **Stop-AzureRmWebApp** stoppar en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="e32fb-108">The **Stop-AzureRmWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="e32fb-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e32fb-109">EXAMPLES</span></span>

### <span data-ttu-id="e32fb-110">Exempel 1: stoppa ett webb program</span><span class="sxs-lookup"><span data-stu-id="e32fb-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="e32fb-111">Det här kommandot stoppar webb programmet som heter ContosoWebApp som tillhör resurs gruppen som heter default-West-väst.</span><span class="sxs-lookup"><span data-stu-id="e32fb-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="e32fb-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e32fb-112">PARAMETERS</span></span>

### <span data-ttu-id="e32fb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e32fb-113">-DefaultProfile</span></span>
<span data-ttu-id="e32fb-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e32fb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e32fb-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="e32fb-115">-Name</span></span>
<span data-ttu-id="e32fb-116">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="e32fb-116">WebApp Name</span></span>

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

### <span data-ttu-id="e32fb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e32fb-117">-ResourceGroupName</span></span>
<span data-ttu-id="e32fb-118">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="e32fb-118">Resource Group Name</span></span>

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

### <span data-ttu-id="e32fb-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="e32fb-119">-WebApp</span></span>
<span data-ttu-id="e32fb-120">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="e32fb-120">WebApp Object</span></span>

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

### <span data-ttu-id="e32fb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e32fb-121">CommonParameters</span></span>
<span data-ttu-id="e32fb-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e32fb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e32fb-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e32fb-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e32fb-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e32fb-124">INPUTS</span></span>

### <span data-ttu-id="e32fb-125">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="e32fb-125">Site</span></span>
<span data-ttu-id="e32fb-126">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="e32fb-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="e32fb-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e32fb-127">OUTPUTS</span></span>

## <span data-ttu-id="e32fb-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e32fb-128">NOTES</span></span>

## <span data-ttu-id="e32fb-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e32fb-129">RELATED LINKS</span></span>

[<span data-ttu-id="e32fb-130">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="e32fb-130">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="e32fb-131">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="e32fb-131">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="e32fb-132">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="e32fb-132">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="e32fb-133">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="e32fb-133">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="e32fb-134">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="e32fb-134">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)


