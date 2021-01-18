---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
ms.openlocfilehash: 4bd0e45df7f1c5c98b61f7f490a59a4c305c2c21
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522116"
---
# <span data-ttu-id="30af4-101">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="30af4-101">Get-AzWebAppSlot</span></span>

## <span data-ttu-id="30af4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="30af4-102">SYNOPSIS</span></span>
<span data-ttu-id="30af4-103">Hämtar en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="30af4-103">Gets an Azure Web App slot.</span></span>

## <span data-ttu-id="30af4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="30af4-104">SYNTAX</span></span>

### <span data-ttu-id="30af4-105">S</span><span class="sxs-lookup"><span data-stu-id="30af4-105">S1</span></span>
```
Get-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30af4-106">S2</span><span class="sxs-lookup"><span data-stu-id="30af4-106">S2</span></span>
```
Get-AzWebAppSlot [[-Slot] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="30af4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="30af4-107">DESCRIPTION</span></span>
<span data-ttu-id="30af4-108">Cmdleten **Get-AzWebAppSlot** hämtar information om en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="30af4-108">The **Get-AzWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="30af4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="30af4-109">EXAMPLES</span></span>

### <span data-ttu-id="30af4-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="30af4-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="30af4-111">Med det här kommandot får du den plats som heter Slot001 från webb programmet som heter WebAppStandard som tillhör resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="30af4-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="30af4-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="30af4-112">PARAMETERS</span></span>

### <span data-ttu-id="30af4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30af4-113">-DefaultProfile</span></span>
<span data-ttu-id="30af4-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="30af4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30af4-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="30af4-115">-Name</span></span>
<span data-ttu-id="30af4-116">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="30af4-116">WebApp Name</span></span>

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

### <span data-ttu-id="30af4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30af4-117">-ResourceGroupName</span></span>
<span data-ttu-id="30af4-118">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="30af4-118">Resource Group Name</span></span>

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

### <span data-ttu-id="30af4-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="30af4-119">-Slot</span></span>
<span data-ttu-id="30af4-120">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="30af4-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="30af4-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="30af4-121">-WebApp</span></span>
<span data-ttu-id="30af4-122">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="30af4-122">WebApp Object</span></span>

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

### <span data-ttu-id="30af4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30af4-123">CommonParameters</span></span>
<span data-ttu-id="30af4-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30af4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30af4-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30af4-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30af4-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="30af4-126">INPUTS</span></span>

### <span data-ttu-id="30af4-127">System. String</span><span class="sxs-lookup"><span data-stu-id="30af4-127">System.String</span></span>

### <span data-ttu-id="30af4-128">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="30af4-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="30af4-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="30af4-129">OUTPUTS</span></span>

### <span data-ttu-id="30af4-130">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="30af4-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="30af4-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="30af4-131">NOTES</span></span>

## <span data-ttu-id="30af4-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="30af4-132">RELATED LINKS</span></span>

[<span data-ttu-id="30af4-133">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="30af4-133">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="30af4-134">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="30af4-134">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="30af4-135">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="30af4-135">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="30af4-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="30af4-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="30af4-137">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="30af4-137">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="30af4-138">Stopp-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="30af4-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="30af4-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="30af4-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
