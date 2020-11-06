---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/start-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebApp.md
ms.openlocfilehash: 74f0fcfdcbbc71781debef62becb36018ecb51a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573135"
---
# <span data-ttu-id="2d0af-101">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2d0af-101">Start-AzureRmWebApp</span></span>

## <span data-ttu-id="2d0af-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2d0af-102">SYNOPSIS</span></span>
<span data-ttu-id="2d0af-103">Startar en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="2d0af-103">Starts an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d0af-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2d0af-104">SYNTAX</span></span>

### <span data-ttu-id="2d0af-105">S</span><span class="sxs-lookup"><span data-stu-id="2d0af-105">S1</span></span>
```
Start-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2d0af-106">S2</span><span class="sxs-lookup"><span data-stu-id="2d0af-106">S2</span></span>
```
Start-AzureRmWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d0af-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2d0af-107">DESCRIPTION</span></span>
<span data-ttu-id="2d0af-108">Cmdleten **Start-AzureRmWebApp** startar en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="2d0af-108">The **Start-AzureRmWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="2d0af-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2d0af-109">EXAMPLES</span></span>

### <span data-ttu-id="2d0af-110">Exempel 1: starta ett webb program</span><span class="sxs-lookup"><span data-stu-id="2d0af-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="2d0af-111">Det här kommandot startar webb programmet som heter ContosoWebApp som tillhör resurs gruppen som heter default-West-väst.</span><span class="sxs-lookup"><span data-stu-id="2d0af-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="2d0af-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2d0af-112">PARAMETERS</span></span>

### <span data-ttu-id="2d0af-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d0af-113">-DefaultProfile</span></span>
<span data-ttu-id="2d0af-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2d0af-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d0af-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="2d0af-115">-Name</span></span>
<span data-ttu-id="2d0af-116">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="2d0af-116">WebApp Name</span></span>

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

### <span data-ttu-id="2d0af-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d0af-117">-ResourceGroupName</span></span>
<span data-ttu-id="2d0af-118">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="2d0af-118">Resource Group Name</span></span>

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

### <span data-ttu-id="2d0af-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="2d0af-119">-WebApp</span></span>
<span data-ttu-id="2d0af-120">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="2d0af-120">WebApp Object</span></span>

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

### <span data-ttu-id="2d0af-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d0af-121">CommonParameters</span></span>
<span data-ttu-id="2d0af-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d0af-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d0af-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d0af-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d0af-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2d0af-124">INPUTS</span></span>

### <span data-ttu-id="2d0af-125">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="2d0af-125">Site</span></span>
<span data-ttu-id="2d0af-126">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="2d0af-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="2d0af-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2d0af-127">OUTPUTS</span></span>

## <span data-ttu-id="2d0af-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2d0af-128">NOTES</span></span>

## <span data-ttu-id="2d0af-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2d0af-129">RELATED LINKS</span></span>

[<span data-ttu-id="2d0af-130">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2d0af-130">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="2d0af-131">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2d0af-131">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="2d0af-132">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2d0af-132">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="2d0af-133">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2d0af-133">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="2d0af-134">Stopp-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2d0af-134">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


