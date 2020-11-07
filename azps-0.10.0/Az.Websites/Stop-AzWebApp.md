---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/stop-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Stop-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Stop-AzWebApp.md
ms.openlocfilehash: 073c98abe9db8b8a8d52c6d9bb06e64b028d379b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923222"
---
# <span data-ttu-id="44aa7-101">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="44aa7-101">Stop-AzWebApp</span></span>

## <span data-ttu-id="44aa7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="44aa7-102">SYNOPSIS</span></span>
<span data-ttu-id="44aa7-103">Stoppar en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="44aa7-103">Stops an Azure Web App.</span></span>

## <span data-ttu-id="44aa7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="44aa7-104">SYNTAX</span></span>

### <span data-ttu-id="44aa7-105">S</span><span class="sxs-lookup"><span data-stu-id="44aa7-105">S1</span></span>
```
Stop-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="44aa7-106">S2</span><span class="sxs-lookup"><span data-stu-id="44aa7-106">S2</span></span>
```
Stop-AzWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44aa7-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="44aa7-107">DESCRIPTION</span></span>
<span data-ttu-id="44aa7-108">Cmdleten **Stop-AzWebApp** stoppar en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="44aa7-108">The **Stop-AzWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="44aa7-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="44aa7-109">EXAMPLES</span></span>

### <span data-ttu-id="44aa7-110">Exempel 1: stoppa ett webb program</span><span class="sxs-lookup"><span data-stu-id="44aa7-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="44aa7-111">Det här kommandot stoppar webb programmet som heter ContosoWebApp som tillhör resurs gruppen som heter default-West-väst.</span><span class="sxs-lookup"><span data-stu-id="44aa7-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="44aa7-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="44aa7-112">PARAMETERS</span></span>

### <span data-ttu-id="44aa7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44aa7-113">-DefaultProfile</span></span>
<span data-ttu-id="44aa7-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="44aa7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44aa7-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="44aa7-115">-Name</span></span>
<span data-ttu-id="44aa7-116">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="44aa7-116">WebApp Name</span></span>

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

### <span data-ttu-id="44aa7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44aa7-117">-ResourceGroupName</span></span>
<span data-ttu-id="44aa7-118">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="44aa7-118">Resource Group Name</span></span>

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

### <span data-ttu-id="44aa7-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="44aa7-119">-WebApp</span></span>
<span data-ttu-id="44aa7-120">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="44aa7-120">WebApp Object</span></span>

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

### <span data-ttu-id="44aa7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44aa7-121">CommonParameters</span></span>
<span data-ttu-id="44aa7-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44aa7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44aa7-123">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44aa7-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44aa7-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="44aa7-124">INPUTS</span></span>

### <span data-ttu-id="44aa7-125">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="44aa7-125">Site</span></span>
<span data-ttu-id="44aa7-126">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="44aa7-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="44aa7-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="44aa7-127">OUTPUTS</span></span>

## <span data-ttu-id="44aa7-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="44aa7-128">NOTES</span></span>

## <span data-ttu-id="44aa7-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="44aa7-129">RELATED LINKS</span></span>

[<span data-ttu-id="44aa7-130">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="44aa7-130">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="44aa7-131">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="44aa7-131">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="44aa7-132">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="44aa7-132">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="44aa7-133">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="44aa7-133">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="44aa7-134">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="44aa7-134">Start-AzWebApp</span></span>](./Start-AzWebApp.md)


