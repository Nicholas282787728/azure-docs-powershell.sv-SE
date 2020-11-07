---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 297071E5-FC06-4493-BCC2-37D4929E4025
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restart-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebApp.md
ms.openlocfilehash: 7543a1dfbbab0c2cedc59fd8ca0d3b60d78ca69d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755362"
---
# <span data-ttu-id="bb943-101">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="bb943-101">Restart-AzureRmWebApp</span></span>

## <span data-ttu-id="bb943-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bb943-102">SYNOPSIS</span></span>
<span data-ttu-id="bb943-103">Startar om en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="bb943-103">Restarts an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb943-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bb943-104">SYNTAX</span></span>

### <span data-ttu-id="bb943-105">S</span><span class="sxs-lookup"><span data-stu-id="bb943-105">S1</span></span>
```
Restart-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bb943-106">S2</span><span class="sxs-lookup"><span data-stu-id="bb943-106">S2</span></span>
```
Restart-AzureRmWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb943-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bb943-107">DESCRIPTION</span></span>
<span data-ttu-id="bb943-108">Cmdleten **restart-AzureRmWebApp** stoppar och startar sedan en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="bb943-108">The **Restart-AzureRmWebApp** cmdlet stops and then starts an Azure Web App.</span></span>
<span data-ttu-id="bb943-109">Om webb programmet är i ett stoppat tillstånd kan du använda Start-AzureRmWebApp cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb943-109">If the Web App is in a stopped state, use the Start-AzureRmWebApp cmdlet.</span></span>

## <span data-ttu-id="bb943-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bb943-110">EXAMPLES</span></span>

### <span data-ttu-id="bb943-111">Exempel 1: starta om ett webb program</span><span class="sxs-lookup"><span data-stu-id="bb943-111">Example 1: Restart a Web App</span></span>
```
PS C:\>Restart-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="bb943-112">Det här kommandot stoppar Azure Web App som heter ContosoSite som tillhör resurs gruppen med namnet default-Web-West och startar sedan om den.</span><span class="sxs-lookup"><span data-stu-id="bb943-112">This command stops the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS and then restarts it.</span></span>

## <span data-ttu-id="bb943-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bb943-113">PARAMETERS</span></span>

### <span data-ttu-id="bb943-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb943-114">-DefaultProfile</span></span>
<span data-ttu-id="bb943-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bb943-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb943-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="bb943-116">-Name</span></span>
<span data-ttu-id="bb943-117">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="bb943-117">WebApp Name</span></span>

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

### <span data-ttu-id="bb943-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb943-118">-ResourceGroupName</span></span>
<span data-ttu-id="bb943-119">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="bb943-119">Resource Group Name</span></span>

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

### <span data-ttu-id="bb943-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="bb943-120">-WebApp</span></span>
<span data-ttu-id="bb943-121">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="bb943-121">WebApp Object</span></span>

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

### <span data-ttu-id="bb943-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb943-122">CommonParameters</span></span>
<span data-ttu-id="bb943-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb943-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb943-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb943-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb943-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bb943-125">INPUTS</span></span>

### <span data-ttu-id="bb943-126">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="bb943-126">Site</span></span>
<span data-ttu-id="bb943-127">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="bb943-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="bb943-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bb943-128">OUTPUTS</span></span>

## <span data-ttu-id="bb943-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bb943-129">NOTES</span></span>

## <span data-ttu-id="bb943-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bb943-130">RELATED LINKS</span></span>

[<span data-ttu-id="bb943-131">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="bb943-131">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="bb943-132">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="bb943-132">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="bb943-133">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="bb943-133">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="bb943-134">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="bb943-134">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="bb943-135">Stopp-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="bb943-135">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


