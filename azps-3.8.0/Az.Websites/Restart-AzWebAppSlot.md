---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restart-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebAppSlot.md
ms.openlocfilehash: 377e08f344256f6d744fec66f0b6b20f495d9309
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090639"
---
# <span data-ttu-id="534e0-101">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="534e0-101">Restart-AzWebAppSlot</span></span>

## <span data-ttu-id="534e0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="534e0-102">SYNOPSIS</span></span>

## <span data-ttu-id="534e0-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="534e0-103">SYNTAX</span></span>

### <span data-ttu-id="534e0-104">S</span><span class="sxs-lookup"><span data-stu-id="534e0-104">S1</span></span>
```
Restart-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="534e0-105">S2</span><span class="sxs-lookup"><span data-stu-id="534e0-105">S2</span></span>
```
Restart-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="534e0-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="534e0-106">DESCRIPTION</span></span>
<span data-ttu-id="534e0-107">Cmdleten **restart-AzWebAppSlot** stoppar och startar sedan en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="534e0-107">The **Restart-AzWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="534e0-108">Om Web App-platsen är i ett stoppat tillstånd kan du använda Start-AzWebAppSlot cmdlet.</span><span class="sxs-lookup"><span data-stu-id="534e0-108">If the Web App Slot is in a stopped state, use the Start-AzWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="534e0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="534e0-109">EXAMPLES</span></span>

### <span data-ttu-id="534e0-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="534e0-110">Example 1</span></span>
```
PS C:\> Restart-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="534e0-111">Det här kommandot startar om fack Slot001 för Web App-ContosoWebApp som är kopplat till resurs gruppens standard-väst</span><span class="sxs-lookup"><span data-stu-id="534e0-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="534e0-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="534e0-112">PARAMETERS</span></span>

### <span data-ttu-id="534e0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="534e0-113">-DefaultProfile</span></span>
<span data-ttu-id="534e0-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="534e0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="534e0-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="534e0-115">-Name</span></span>
<span data-ttu-id="534e0-116">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="534e0-116">WebApp Name</span></span>

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

### <span data-ttu-id="534e0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="534e0-117">-ResourceGroupName</span></span>
<span data-ttu-id="534e0-118">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="534e0-118">Resource Group Name</span></span>

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

### <span data-ttu-id="534e0-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="534e0-119">-Slot</span></span>
<span data-ttu-id="534e0-120">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="534e0-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="534e0-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="534e0-121">-WebApp</span></span>
<span data-ttu-id="534e0-122">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="534e0-122">WebApp Object</span></span>

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

### <span data-ttu-id="534e0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="534e0-123">CommonParameters</span></span>
<span data-ttu-id="534e0-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="534e0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="534e0-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="534e0-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="534e0-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="534e0-126">INPUTS</span></span>

### <span data-ttu-id="534e0-127">System. String</span><span class="sxs-lookup"><span data-stu-id="534e0-127">System.String</span></span>

### <span data-ttu-id="534e0-128">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="534e0-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="534e0-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="534e0-129">OUTPUTS</span></span>

### <span data-ttu-id="534e0-130">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="534e0-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="534e0-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="534e0-131">NOTES</span></span>

## <span data-ttu-id="534e0-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="534e0-132">RELATED LINKS</span></span>

[<span data-ttu-id="534e0-133">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="534e0-133">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="534e0-134">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="534e0-134">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="534e0-135">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="534e0-135">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="534e0-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="534e0-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="534e0-137">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="534e0-137">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="534e0-138">Stopp-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="534e0-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="534e0-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="534e0-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
