---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/start-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Start-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Start-AzWebApp.md
ms.openlocfilehash: d533a2d7401236e374ca6f541e646cb85a080f9b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923250"
---
# <span data-ttu-id="00ea4-101">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="00ea4-101">Start-AzWebApp</span></span>

## <span data-ttu-id="00ea4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="00ea4-102">SYNOPSIS</span></span>
<span data-ttu-id="00ea4-103">Startar en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="00ea4-103">Starts an Azure Web App.</span></span>

## <span data-ttu-id="00ea4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="00ea4-104">SYNTAX</span></span>

### <span data-ttu-id="00ea4-105">S</span><span class="sxs-lookup"><span data-stu-id="00ea4-105">S1</span></span>
```
Start-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="00ea4-106">S2</span><span class="sxs-lookup"><span data-stu-id="00ea4-106">S2</span></span>
```
Start-AzWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00ea4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="00ea4-107">DESCRIPTION</span></span>
<span data-ttu-id="00ea4-108">Cmdleten **Start-AzWebApp** startar en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="00ea4-108">The **Start-AzWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="00ea4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="00ea4-109">EXAMPLES</span></span>

### <span data-ttu-id="00ea4-110">Exempel 1: starta ett webb program</span><span class="sxs-lookup"><span data-stu-id="00ea4-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="00ea4-111">Det här kommandot startar webb programmet som heter ContosoWebApp som tillhör resurs gruppen som heter default-West-väst.</span><span class="sxs-lookup"><span data-stu-id="00ea4-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="00ea4-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="00ea4-112">PARAMETERS</span></span>

### <span data-ttu-id="00ea4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00ea4-113">-DefaultProfile</span></span>
<span data-ttu-id="00ea4-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="00ea4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00ea4-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="00ea4-115">-Name</span></span>
<span data-ttu-id="00ea4-116">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="00ea4-116">WebApp Name</span></span>

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

### <span data-ttu-id="00ea4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00ea4-117">-ResourceGroupName</span></span>
<span data-ttu-id="00ea4-118">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="00ea4-118">Resource Group Name</span></span>

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

### <span data-ttu-id="00ea4-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="00ea4-119">-WebApp</span></span>
<span data-ttu-id="00ea4-120">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="00ea4-120">WebApp Object</span></span>

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

### <span data-ttu-id="00ea4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00ea4-121">CommonParameters</span></span>
<span data-ttu-id="00ea4-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00ea4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00ea4-123">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00ea4-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00ea4-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="00ea4-124">INPUTS</span></span>

### <span data-ttu-id="00ea4-125">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="00ea4-125">Site</span></span>
<span data-ttu-id="00ea4-126">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="00ea4-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="00ea4-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="00ea4-127">OUTPUTS</span></span>

## <span data-ttu-id="00ea4-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="00ea4-128">NOTES</span></span>

## <span data-ttu-id="00ea4-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="00ea4-129">RELATED LINKS</span></span>

[<span data-ttu-id="00ea4-130">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="00ea4-130">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="00ea4-131">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="00ea4-131">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="00ea4-132">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="00ea4-132">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="00ea4-133">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="00ea4-133">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="00ea4-134">Stopp-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="00ea4-134">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


