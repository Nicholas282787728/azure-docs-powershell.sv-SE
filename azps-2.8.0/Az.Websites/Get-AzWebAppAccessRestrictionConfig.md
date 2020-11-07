---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: 49d79edf08db218149798e832f3706c0eb4697cd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93921128"
---
# <span data-ttu-id="c4db1-101">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="c4db1-101">Get-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="c4db1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c4db1-102">SYNOPSIS</span></span>
<span data-ttu-id="c4db1-103">Hämtar Restiction-konfiguration för ett Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="c4db1-103">Gets Access Restiction configuration for an Azure Web App.</span></span>

## <span data-ttu-id="c4db1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c4db1-104">SYNTAX</span></span>

```
Get-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String> [[-SlotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4db1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c4db1-105">DESCRIPTION</span></span>
<span data-ttu-id="c4db1-106">Cmdleten **Get-AzWebAppAccessRestrictionConfig** får åtkomst begränsnings konfiguration för Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="c4db1-106">The **Get-AzWebAppAccessRestrictionConfig** cmdlet gets Access Restriction config about an Azure Web App.</span></span>

## <span data-ttu-id="c4db1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c4db1-107">EXAMPLES</span></span>

### <span data-ttu-id="c4db1-108">Exempel 1: Hämta en begränsning för åtkomst begränsningar för webb program från en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="c4db1-108">Example 1: Get a Web App Access Restriction Config from a resource group</span></span>
```
PS C:\>Get-AzWebAppAccessRestrictionConfig -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="c4db1-109">Det här kommandot får åtkomst begränsningen config för ett webb program som heter ContosoSite som tillhör resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="c4db1-109">This command gets the access restriction config of a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="c4db1-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c4db1-110">PARAMETERS</span></span>

### <span data-ttu-id="c4db1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4db1-111">-DefaultProfile</span></span>
<span data-ttu-id="c4db1-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c4db1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4db1-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="c4db1-113">-Name</span></span>
<span data-ttu-id="c4db1-114">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="c4db1-114">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4db1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4db1-115">-ResourceGroupName</span></span>
<span data-ttu-id="c4db1-116">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="c4db1-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4db1-117">-SlotName</span><span class="sxs-lookup"><span data-stu-id="c4db1-117">-SlotName</span></span>
<span data-ttu-id="c4db1-118">Namn på distributions platsen.</span><span class="sxs-lookup"><span data-stu-id="c4db1-118">Deployment Slot name.</span></span>

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

### <span data-ttu-id="c4db1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4db1-119">CommonParameters</span></span>
<span data-ttu-id="c4db1-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4db1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4db1-121">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c4db1-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4db1-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c4db1-122">INPUTS</span></span>

### <span data-ttu-id="c4db1-123">System. String</span><span class="sxs-lookup"><span data-stu-id="c4db1-123">System.String</span></span>

## <span data-ttu-id="c4db1-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c4db1-124">OUTPUTS</span></span>

### <span data-ttu-id="c4db1-125">Microsoft. Azure. commands. webapps. Models. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="c4db1-125">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="c4db1-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c4db1-126">NOTES</span></span>

## <span data-ttu-id="c4db1-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c4db1-127">RELATED LINKS</span></span>

[<span data-ttu-id="c4db1-128">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="c4db1-128">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="c4db1-129">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="c4db1-129">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="c4db1-130">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="c4db1-130">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
