---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlot.md
ms.openlocfilehash: f7be5b7877362484d0f3dfe4d19b8afc669e917c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572560"
---
# <span data-ttu-id="a4ec0-101">Get-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a4ec0-101">Get-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="a4ec0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a4ec0-102">SYNOPSIS</span></span>
<span data-ttu-id="a4ec0-103">Hämtar en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="a4ec0-103">Gets an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4ec0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a4ec0-104">SYNTAX</span></span>

### <span data-ttu-id="a4ec0-105">S</span><span class="sxs-lookup"><span data-stu-id="a4ec0-105">S1</span></span>
```
Get-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4ec0-106">S2</span><span class="sxs-lookup"><span data-stu-id="a4ec0-106">S2</span></span>
```
Get-AzureRmWebAppSlot [[-Slot] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4ec0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a4ec0-107">DESCRIPTION</span></span>
<span data-ttu-id="a4ec0-108">Cmdleten **Get-AzureRmWebAppSlot** hämtar information om en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="a4ec0-108">The **Get-AzureRmWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="a4ec0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a4ec0-109">EXAMPLES</span></span>

### <span data-ttu-id="a4ec0-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a4ec0-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="a4ec0-111">Med det här kommandot får du den plats som heter Slot001 från webb programmet som heter WebAppStandard som tillhör resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="a4ec0-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="a4ec0-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a4ec0-112">PARAMETERS</span></span>

### <span data-ttu-id="a4ec0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4ec0-113">-DefaultProfile</span></span>
<span data-ttu-id="a4ec0-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a4ec0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4ec0-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="a4ec0-115">-Name</span></span>
<span data-ttu-id="a4ec0-116">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="a4ec0-116">WebApp Name</span></span>

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

### <span data-ttu-id="a4ec0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4ec0-117">-ResourceGroupName</span></span>
<span data-ttu-id="a4ec0-118">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="a4ec0-118">Resource Group Name</span></span>

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

### <span data-ttu-id="a4ec0-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="a4ec0-119">-Slot</span></span>
<span data-ttu-id="a4ec0-120">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="a4ec0-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="a4ec0-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="a4ec0-121">-WebApp</span></span>
<span data-ttu-id="a4ec0-122">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="a4ec0-122">WebApp Object</span></span>

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

### <span data-ttu-id="a4ec0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4ec0-123">CommonParameters</span></span>
<span data-ttu-id="a4ec0-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4ec0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4ec0-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4ec0-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4ec0-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a4ec0-126">INPUTS</span></span>

### <span data-ttu-id="a4ec0-127">System. String</span><span class="sxs-lookup"><span data-stu-id="a4ec0-127">System.String</span></span>

### <span data-ttu-id="a4ec0-128">Microsoft. Azure. Management. webbplatser. Models. site</span><span class="sxs-lookup"><span data-stu-id="a4ec0-128">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="a4ec0-129">Parametrar: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a4ec0-129">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="a4ec0-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a4ec0-130">OUTPUTS</span></span>

### <span data-ttu-id="a4ec0-131">Microsoft. Azure. Management. webbplatser. Models. site</span><span class="sxs-lookup"><span data-stu-id="a4ec0-131">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="a4ec0-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a4ec0-132">NOTES</span></span>

## <span data-ttu-id="a4ec0-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a4ec0-133">RELATED LINKS</span></span>

[<span data-ttu-id="a4ec0-134">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a4ec0-134">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="a4ec0-135">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a4ec0-135">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="a4ec0-136">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a4ec0-136">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="a4ec0-137">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a4ec0-137">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="a4ec0-138">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a4ec0-138">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="a4ec0-139">Stopp-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a4ec0-139">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="a4ec0-140">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="a4ec0-140">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
