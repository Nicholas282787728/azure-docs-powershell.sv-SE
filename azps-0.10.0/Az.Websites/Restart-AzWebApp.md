---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 297071E5-FC06-4493-BCC2-37D4929E4025
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/restart-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restart-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restart-AzWebApp.md
ms.openlocfilehash: 975b49af1e20c5b9f4839a561494eaeb8275f02f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923269"
---
# <span data-ttu-id="c25b4-101">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c25b4-101">Restart-AzWebApp</span></span>

## <span data-ttu-id="c25b4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c25b4-102">SYNOPSIS</span></span>
<span data-ttu-id="c25b4-103">Startar om en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="c25b4-103">Restarts an Azure Web App.</span></span>

## <span data-ttu-id="c25b4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c25b4-104">SYNTAX</span></span>

### <span data-ttu-id="c25b4-105">S</span><span class="sxs-lookup"><span data-stu-id="c25b4-105">S1</span></span>
```
Restart-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c25b4-106">S2</span><span class="sxs-lookup"><span data-stu-id="c25b4-106">S2</span></span>
```
Restart-AzWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c25b4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c25b4-107">DESCRIPTION</span></span>
<span data-ttu-id="c25b4-108">Cmdleten **restart-AzWebApp** stoppar och startar sedan en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="c25b4-108">The **Restart-AzWebApp** cmdlet stops and then starts an Azure Web App.</span></span>
<span data-ttu-id="c25b4-109">Om webb programmet är i ett stoppat tillstånd kan du använda Start-AzWebApp cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c25b4-109">If the Web App is in a stopped state, use the Start-AzWebApp cmdlet.</span></span>

## <span data-ttu-id="c25b4-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c25b4-110">EXAMPLES</span></span>

### <span data-ttu-id="c25b4-111">Exempel 1: starta om ett webb program</span><span class="sxs-lookup"><span data-stu-id="c25b4-111">Example 1: Restart a Web App</span></span>
```
PS C:\>Restart-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="c25b4-112">Det här kommandot stoppar Azure Web App som heter ContosoSite som tillhör resurs gruppen med namnet default-Web-West och startar sedan om den.</span><span class="sxs-lookup"><span data-stu-id="c25b4-112">This command stops the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS and then restarts it.</span></span>

## <span data-ttu-id="c25b4-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c25b4-113">PARAMETERS</span></span>

### <span data-ttu-id="c25b4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c25b4-114">-DefaultProfile</span></span>
<span data-ttu-id="c25b4-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c25b4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c25b4-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="c25b4-116">-Name</span></span>
<span data-ttu-id="c25b4-117">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="c25b4-117">WebApp Name</span></span>

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

### <span data-ttu-id="c25b4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c25b4-118">-ResourceGroupName</span></span>
<span data-ttu-id="c25b4-119">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="c25b4-119">Resource Group Name</span></span>

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

### <span data-ttu-id="c25b4-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c25b4-120">-WebApp</span></span>
<span data-ttu-id="c25b4-121">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="c25b4-121">WebApp Object</span></span>

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

### <span data-ttu-id="c25b4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c25b4-122">CommonParameters</span></span>
<span data-ttu-id="c25b4-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c25b4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c25b4-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c25b4-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c25b4-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c25b4-125">INPUTS</span></span>

### <span data-ttu-id="c25b4-126">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="c25b4-126">Site</span></span>
<span data-ttu-id="c25b4-127">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="c25b4-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="c25b4-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c25b4-128">OUTPUTS</span></span>

## <span data-ttu-id="c25b4-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c25b4-129">NOTES</span></span>

## <span data-ttu-id="c25b4-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c25b4-130">RELATED LINKS</span></span>

[<span data-ttu-id="c25b4-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c25b4-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="c25b4-132">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c25b4-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="c25b4-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c25b4-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="c25b4-134">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c25b4-134">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="c25b4-135">Stopp-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c25b4-135">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


