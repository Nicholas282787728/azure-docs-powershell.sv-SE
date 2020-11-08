---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 297071E5-FC06-4493-BCC2-37D4929E4025
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restart-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebApp.md
ms.openlocfilehash: faa3264dbf9fa65a2970f578c635868d185f2ef8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258427"
---
# <span data-ttu-id="0da3b-101">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0da3b-101">Restart-AzWebApp</span></span>

## <span data-ttu-id="0da3b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0da3b-102">SYNOPSIS</span></span>
<span data-ttu-id="0da3b-103">Startar om en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="0da3b-103">Restarts an Azure Web App.</span></span>

## <span data-ttu-id="0da3b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0da3b-104">SYNTAX</span></span>

### <span data-ttu-id="0da3b-105">S</span><span class="sxs-lookup"><span data-stu-id="0da3b-105">S1</span></span>
```
Restart-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0da3b-106">S2</span><span class="sxs-lookup"><span data-stu-id="0da3b-106">S2</span></span>
```
Restart-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0da3b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0da3b-107">DESCRIPTION</span></span>
<span data-ttu-id="0da3b-108">Cmdleten **restart-AzWebApp** stoppar och startar sedan en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="0da3b-108">The **Restart-AzWebApp** cmdlet stops and then starts an Azure Web App.</span></span>
<span data-ttu-id="0da3b-109">Om webb programmet är i ett stoppat tillstånd kan du använda Start-AzWebApp cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0da3b-109">If the Web App is in a stopped state, use the Start-AzWebApp cmdlet.</span></span>

## <span data-ttu-id="0da3b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0da3b-110">EXAMPLES</span></span>

### <span data-ttu-id="0da3b-111">Exempel 1: starta om ett webb program</span><span class="sxs-lookup"><span data-stu-id="0da3b-111">Example 1: Restart a Web App</span></span>
```
PS C:\>Restart-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="0da3b-112">Det här kommandot stoppar Azure Web App som heter ContosoSite som tillhör resurs gruppen med namnet default-Web-West och startar sedan om den.</span><span class="sxs-lookup"><span data-stu-id="0da3b-112">This command stops the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS and then restarts it.</span></span>

## <span data-ttu-id="0da3b-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0da3b-113">PARAMETERS</span></span>

### <span data-ttu-id="0da3b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0da3b-114">-DefaultProfile</span></span>
<span data-ttu-id="0da3b-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0da3b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0da3b-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="0da3b-116">-Name</span></span>
<span data-ttu-id="0da3b-117">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="0da3b-117">WebApp Name</span></span>

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

### <span data-ttu-id="0da3b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0da3b-118">-ResourceGroupName</span></span>
<span data-ttu-id="0da3b-119">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="0da3b-119">Resource Group Name</span></span>

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

### <span data-ttu-id="0da3b-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="0da3b-120">-WebApp</span></span>
<span data-ttu-id="0da3b-121">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="0da3b-121">WebApp Object</span></span>

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

### <span data-ttu-id="0da3b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0da3b-122">CommonParameters</span></span>
<span data-ttu-id="0da3b-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0da3b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0da3b-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0da3b-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0da3b-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0da3b-125">INPUTS</span></span>

### <span data-ttu-id="0da3b-126">System. String</span><span class="sxs-lookup"><span data-stu-id="0da3b-126">System.String</span></span>

### <span data-ttu-id="0da3b-127">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="0da3b-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="0da3b-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0da3b-128">OUTPUTS</span></span>

### <span data-ttu-id="0da3b-129">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="0da3b-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="0da3b-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0da3b-130">NOTES</span></span>

## <span data-ttu-id="0da3b-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0da3b-131">RELATED LINKS</span></span>

[<span data-ttu-id="0da3b-132">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0da3b-132">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="0da3b-133">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0da3b-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="0da3b-134">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0da3b-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="0da3b-135">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0da3b-135">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="0da3b-136">Stopp-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0da3b-136">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


