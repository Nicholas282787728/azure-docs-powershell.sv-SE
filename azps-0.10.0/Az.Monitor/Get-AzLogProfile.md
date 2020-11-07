---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzLogProfile.md
ms.openlocfilehash: 5d99bafdd011409eae322c60db6e596d3c77cd4f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922617"
---
# <span data-ttu-id="290d8-101">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="290d8-101">Get-AzLogProfile</span></span>

## <span data-ttu-id="290d8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="290d8-102">SYNOPSIS</span></span>
<span data-ttu-id="290d8-103">Hämtar en logg profil.</span><span class="sxs-lookup"><span data-stu-id="290d8-103">Gets a log profile.</span></span>

## <span data-ttu-id="290d8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="290d8-104">SYNTAX</span></span>

```
Get-AzLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="290d8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="290d8-105">DESCRIPTION</span></span>
<span data-ttu-id="290d8-106">Cmdleten **Get-AzLogProfile** hämtar en logg profil.</span><span class="sxs-lookup"><span data-stu-id="290d8-106">The **Get-AzLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="290d8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="290d8-107">EXAMPLES</span></span>

## <span data-ttu-id="290d8-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="290d8-108">PARAMETERS</span></span>

### <span data-ttu-id="290d8-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="290d8-109">-DefaultProfile</span></span>
<span data-ttu-id="290d8-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="290d8-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="290d8-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="290d8-111">-Name</span></span>
<span data-ttu-id="290d8-112">Anger namnet på den logg profil som ska visas.</span><span class="sxs-lookup"><span data-stu-id="290d8-112">Specifies the name of the log profile to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="290d8-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="290d8-113">CommonParameters</span></span>
<span data-ttu-id="290d8-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="290d8-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="290d8-115">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="290d8-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="290d8-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="290d8-116">INPUTS</span></span>

### <span data-ttu-id="290d8-117">System. String</span><span class="sxs-lookup"><span data-stu-id="290d8-117">System.String</span></span>

## <span data-ttu-id="290d8-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="290d8-118">OUTPUTS</span></span>

### <span data-ttu-id="290d8-119">Microsoft. Azure. commands. Insights. OutputClasses. PSLogProfileCollection</span><span class="sxs-lookup"><span data-stu-id="290d8-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="290d8-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="290d8-120">NOTES</span></span>

## <span data-ttu-id="290d8-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="290d8-121">RELATED LINKS</span></span>

[<span data-ttu-id="290d8-122">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="290d8-122">Add-AzLogProfile</span></span>](./Add-AzLogProfile.md)

[<span data-ttu-id="290d8-123">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="290d8-123">Remove-AzLogProfile</span></span>](./Remove-AzLogProfile.md)


