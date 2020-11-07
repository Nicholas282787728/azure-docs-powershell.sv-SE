---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restart-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: ad3ff3dbd5589a890ecf7649c9a9b66843b8b444
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931085"
---
# <span data-ttu-id="a1f87-101">Restart-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a1f87-101">Restart-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="a1f87-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a1f87-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1f87-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a1f87-103">SYNTAX</span></span>

### <span data-ttu-id="a1f87-104">S</span><span class="sxs-lookup"><span data-stu-id="a1f87-104">S1</span></span>
```
Restart-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1f87-105">S2</span><span class="sxs-lookup"><span data-stu-id="a1f87-105">S2</span></span>
```
Restart-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1f87-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a1f87-106">DESCRIPTION</span></span>
<span data-ttu-id="a1f87-107">Cmdleten **restart-AzureRmWebAppSlot** stoppar och startar sedan en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="a1f87-107">The **Restart-AzureRmWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="a1f87-108">Om Web App-platsen är i ett stoppat tillstånd kan du använda Start-AzureRmWebAppSlot cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1f87-108">If the Web App Slot is in a stopped state, use the Start-AzureRmWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="a1f87-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a1f87-109">EXAMPLES</span></span>

### <span data-ttu-id="a1f87-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a1f87-110">Example 1</span></span>
```
PS C:\> Restart-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="a1f87-111">Det här kommandot startar om fack Slot001 för Web App-ContosoWebApp som är kopplat till resurs gruppens standard-väst</span><span class="sxs-lookup"><span data-stu-id="a1f87-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="a1f87-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a1f87-112">PARAMETERS</span></span>

### <span data-ttu-id="a1f87-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1f87-113">-DefaultProfile</span></span>
<span data-ttu-id="a1f87-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a1f87-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1f87-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="a1f87-115">-Name</span></span>
<span data-ttu-id="a1f87-116">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="a1f87-116">WebApp Name</span></span>

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

### <span data-ttu-id="a1f87-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1f87-117">-ResourceGroupName</span></span>
<span data-ttu-id="a1f87-118">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="a1f87-118">Resource Group Name</span></span>

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

### <span data-ttu-id="a1f87-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="a1f87-119">-Slot</span></span>
<span data-ttu-id="a1f87-120">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="a1f87-120">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1f87-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="a1f87-121">-WebApp</span></span>
<span data-ttu-id="a1f87-122">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="a1f87-122">WebApp Object</span></span>

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

### <span data-ttu-id="a1f87-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1f87-123">CommonParameters</span></span>
<span data-ttu-id="a1f87-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1f87-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1f87-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1f87-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1f87-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a1f87-126">INPUTS</span></span>

### <span data-ttu-id="a1f87-127">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="a1f87-127">Site</span></span>
<span data-ttu-id="a1f87-128">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="a1f87-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="a1f87-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a1f87-129">OUTPUTS</span></span>

## <span data-ttu-id="a1f87-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a1f87-130">NOTES</span></span>

## <span data-ttu-id="a1f87-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a1f87-131">RELATED LINKS</span></span>

[<span data-ttu-id="a1f87-132">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a1f87-132">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="a1f87-133">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a1f87-133">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="a1f87-134">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a1f87-134">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="a1f87-135">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a1f87-135">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="a1f87-136">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a1f87-136">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="a1f87-137">Stopp-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a1f87-137">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="a1f87-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="a1f87-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
