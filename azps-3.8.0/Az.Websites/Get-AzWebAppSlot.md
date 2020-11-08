---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
ms.openlocfilehash: 4bd0e45df7f1c5c98b61f7f490a59a4c305c2c21
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089737"
---
# <span data-ttu-id="7c607-101">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7c607-101">Get-AzWebAppSlot</span></span>

## <span data-ttu-id="7c607-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7c607-102">SYNOPSIS</span></span>
<span data-ttu-id="7c607-103">Hämtar en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="7c607-103">Gets an Azure Web App slot.</span></span>

## <span data-ttu-id="7c607-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7c607-104">SYNTAX</span></span>

### <span data-ttu-id="7c607-105">S</span><span class="sxs-lookup"><span data-stu-id="7c607-105">S1</span></span>
```
Get-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c607-106">S2</span><span class="sxs-lookup"><span data-stu-id="7c607-106">S2</span></span>
```
Get-AzWebAppSlot [[-Slot] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7c607-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7c607-107">DESCRIPTION</span></span>
<span data-ttu-id="7c607-108">Cmdleten **Get-AzWebAppSlot** hämtar information om en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="7c607-108">The **Get-AzWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="7c607-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7c607-109">EXAMPLES</span></span>

### <span data-ttu-id="7c607-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7c607-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="7c607-111">Med det här kommandot får du den plats som heter Slot001 från webb programmet som heter WebAppStandard som tillhör resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="7c607-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="7c607-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7c607-112">PARAMETERS</span></span>

### <span data-ttu-id="7c607-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c607-113">-DefaultProfile</span></span>
<span data-ttu-id="7c607-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7c607-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c607-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="7c607-115">-Name</span></span>
<span data-ttu-id="7c607-116">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="7c607-116">WebApp Name</span></span>

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

### <span data-ttu-id="7c607-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c607-117">-ResourceGroupName</span></span>
<span data-ttu-id="7c607-118">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="7c607-118">Resource Group Name</span></span>

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

### <span data-ttu-id="7c607-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="7c607-119">-Slot</span></span>
<span data-ttu-id="7c607-120">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="7c607-120">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c607-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="7c607-121">-WebApp</span></span>
<span data-ttu-id="7c607-122">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="7c607-122">WebApp Object</span></span>

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

### <span data-ttu-id="7c607-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c607-123">CommonParameters</span></span>
<span data-ttu-id="7c607-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c607-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c607-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c607-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c607-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7c607-126">INPUTS</span></span>

### <span data-ttu-id="7c607-127">System. String</span><span class="sxs-lookup"><span data-stu-id="7c607-127">System.String</span></span>

### <span data-ttu-id="7c607-128">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="7c607-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="7c607-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7c607-129">OUTPUTS</span></span>

### <span data-ttu-id="7c607-130">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="7c607-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="7c607-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7c607-131">NOTES</span></span>

## <span data-ttu-id="7c607-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7c607-132">RELATED LINKS</span></span>

[<span data-ttu-id="7c607-133">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7c607-133">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="7c607-134">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7c607-134">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="7c607-135">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7c607-135">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="7c607-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7c607-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="7c607-137">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7c607-137">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="7c607-138">Stopp-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7c607-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="7c607-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7c607-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
