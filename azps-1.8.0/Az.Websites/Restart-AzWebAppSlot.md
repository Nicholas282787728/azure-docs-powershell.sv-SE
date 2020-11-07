---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restart-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebAppSlot.md
ms.openlocfilehash: 53323aaf29145f4340dd00fa752d8afd2dd72131
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746032"
---
# <span data-ttu-id="54c0f-101">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="54c0f-101">Restart-AzWebAppSlot</span></span>

## <span data-ttu-id="54c0f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="54c0f-102">SYNOPSIS</span></span>

## <span data-ttu-id="54c0f-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="54c0f-103">SYNTAX</span></span>

### <span data-ttu-id="54c0f-104">S</span><span class="sxs-lookup"><span data-stu-id="54c0f-104">S1</span></span>
```
Restart-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54c0f-105">S2</span><span class="sxs-lookup"><span data-stu-id="54c0f-105">S2</span></span>
```
Restart-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54c0f-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="54c0f-106">DESCRIPTION</span></span>
<span data-ttu-id="54c0f-107">Cmdleten **restart-AzWebAppSlot** stoppar och startar sedan en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="54c0f-107">The **Restart-AzWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="54c0f-108">Om Web App-platsen är i ett stoppat tillstånd kan du använda Start-AzWebAppSlot cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54c0f-108">If the Web App Slot is in a stopped state, use the Start-AzWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="54c0f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="54c0f-109">EXAMPLES</span></span>

### <span data-ttu-id="54c0f-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="54c0f-110">Example 1</span></span>
```
PS C:\> Restart-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="54c0f-111">Det här kommandot startar om fack Slot001 för Web App-ContosoWebApp som är kopplat till resurs gruppens standard-väst</span><span class="sxs-lookup"><span data-stu-id="54c0f-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="54c0f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="54c0f-112">PARAMETERS</span></span>

### <span data-ttu-id="54c0f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54c0f-113">-DefaultProfile</span></span>
<span data-ttu-id="54c0f-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="54c0f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54c0f-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="54c0f-115">-Name</span></span>
<span data-ttu-id="54c0f-116">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="54c0f-116">WebApp Name</span></span>

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

### <span data-ttu-id="54c0f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54c0f-117">-ResourceGroupName</span></span>
<span data-ttu-id="54c0f-118">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="54c0f-118">Resource Group Name</span></span>

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

### <span data-ttu-id="54c0f-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="54c0f-119">-Slot</span></span>
<span data-ttu-id="54c0f-120">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="54c0f-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="54c0f-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="54c0f-121">-WebApp</span></span>
<span data-ttu-id="54c0f-122">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="54c0f-122">WebApp Object</span></span>

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

### <span data-ttu-id="54c0f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54c0f-123">CommonParameters</span></span>
<span data-ttu-id="54c0f-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54c0f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54c0f-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54c0f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54c0f-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="54c0f-126">INPUTS</span></span>

### <span data-ttu-id="54c0f-127">System. String</span><span class="sxs-lookup"><span data-stu-id="54c0f-127">System.String</span></span>

### <span data-ttu-id="54c0f-128">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="54c0f-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="54c0f-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="54c0f-129">OUTPUTS</span></span>

### <span data-ttu-id="54c0f-130">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="54c0f-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="54c0f-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="54c0f-131">NOTES</span></span>

## <span data-ttu-id="54c0f-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="54c0f-132">RELATED LINKS</span></span>

[<span data-ttu-id="54c0f-133">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="54c0f-133">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="54c0f-134">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="54c0f-134">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="54c0f-135">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="54c0f-135">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="54c0f-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="54c0f-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="54c0f-137">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="54c0f-137">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="54c0f-138">Stopp-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="54c0f-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="54c0f-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="54c0f-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)