---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/start-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebAppSlot.md
ms.openlocfilehash: 4425c344fb0c9e0e3441c172915be11002ee8b1b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090313"
---
# <span data-ttu-id="c3e07-101">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c3e07-101">Start-AzWebAppSlot</span></span>

## <span data-ttu-id="c3e07-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c3e07-102">SYNOPSIS</span></span>
<span data-ttu-id="c3e07-103">Startar en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="c3e07-103">Starts an Azure Web App slot.</span></span>

## <span data-ttu-id="c3e07-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c3e07-104">SYNTAX</span></span>

### <span data-ttu-id="c3e07-105">S</span><span class="sxs-lookup"><span data-stu-id="c3e07-105">S1</span></span>
```
Start-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3e07-106">S2</span><span class="sxs-lookup"><span data-stu-id="c3e07-106">S2</span></span>
```
Start-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3e07-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c3e07-107">DESCRIPTION</span></span>
<span data-ttu-id="c3e07-108">Cmdleten **Start-AzWebAppSlot** startar en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="c3e07-108">The **Start-AzWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="c3e07-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c3e07-109">EXAMPLES</span></span>

### <span data-ttu-id="c3e07-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c3e07-110">Example 1</span></span>
```
PS C:\>Start-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="c3e07-111">Det här kommandot startar facket som heter Slot001 som hör till webb programmet som heter ContosoWebApp och som tillhör resurs gruppen som heter default-West-väst.</span><span class="sxs-lookup"><span data-stu-id="c3e07-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="c3e07-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c3e07-112">PARAMETERS</span></span>

### <span data-ttu-id="c3e07-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3e07-113">-DefaultProfile</span></span>
<span data-ttu-id="c3e07-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c3e07-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3e07-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="c3e07-115">-Name</span></span>
<span data-ttu-id="c3e07-116">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="c3e07-116">WebApp Name</span></span>

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

### <span data-ttu-id="c3e07-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3e07-117">-ResourceGroupName</span></span>
<span data-ttu-id="c3e07-118">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="c3e07-118">Resource Group Name</span></span>

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

### <span data-ttu-id="c3e07-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="c3e07-119">-Slot</span></span>
<span data-ttu-id="c3e07-120">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="c3e07-120">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e07-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c3e07-121">-WebApp</span></span>
<span data-ttu-id="c3e07-122">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="c3e07-122">WebApp Object</span></span>

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

### <span data-ttu-id="c3e07-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3e07-123">CommonParameters</span></span>
<span data-ttu-id="c3e07-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3e07-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3e07-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3e07-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3e07-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c3e07-126">INPUTS</span></span>

### <span data-ttu-id="c3e07-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c3e07-127">System.String</span></span>

### <span data-ttu-id="c3e07-128">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="c3e07-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c3e07-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c3e07-129">OUTPUTS</span></span>

### <span data-ttu-id="c3e07-130">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="c3e07-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c3e07-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c3e07-131">NOTES</span></span>

## <span data-ttu-id="c3e07-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c3e07-132">RELATED LINKS</span></span>

[<span data-ttu-id="c3e07-133">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c3e07-133">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="c3e07-134">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c3e07-134">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="c3e07-135">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c3e07-135">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="c3e07-136">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c3e07-136">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="c3e07-137">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c3e07-137">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="c3e07-138">Stopp-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c3e07-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="c3e07-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c3e07-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
