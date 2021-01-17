---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: 7f84c3b10577eea0d035c2ce84b3aa8a61af4a3d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396059"
---
# <span data-ttu-id="9e4e7-101">Get-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="9e4e7-101">Get-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="9e4e7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9e4e7-102">SYNOPSIS</span></span>
<span data-ttu-id="9e4e7-103">Hämtar den faktiska skydds principen för klient organisationens SQL information.</span><span class="sxs-lookup"><span data-stu-id="9e4e7-103">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="9e4e7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9e4e7-104">SYNTAX</span></span>

```
Get-AzSqlInformationProtectionPolicy [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e4e7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9e4e7-105">DESCRIPTION</span></span>
<span data-ttu-id="9e4e7-106">Hämtar den faktiska skydds principen för klient organisationens SQL information.</span><span class="sxs-lookup"><span data-stu-id="9e4e7-106">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="9e4e7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9e4e7-107">EXAMPLES</span></span>

### <span data-ttu-id="9e4e7-108">Exempel</span><span class="sxs-lookup"><span data-stu-id="9e4e7-108">Example</span></span>
```powershell
PS C:\> Get-AzSqlInformationProtectionPolicy
```

## <span data-ttu-id="9e4e7-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9e4e7-109">PARAMETERS</span></span>

### <span data-ttu-id="9e4e7-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e4e7-110">-AsJob</span></span>
<span data-ttu-id="9e4e7-111">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="9e4e7-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e4e7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e4e7-112">-DefaultProfile</span></span>
<span data-ttu-id="9e4e7-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9e4e7-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e4e7-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e4e7-114">CommonParameters</span></span>
<span data-ttu-id="9e4e7-115">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e4e7-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e4e7-116">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e4e7-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e4e7-117">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9e4e7-117">INPUTS</span></span>

### <span data-ttu-id="9e4e7-118">System. String</span><span class="sxs-lookup"><span data-stu-id="9e4e7-118">System.string</span></span>

## <span data-ttu-id="9e4e7-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9e4e7-119">OUTPUTS</span></span>

### <span data-ttu-id="9e4e7-120">Microsoft. Azure. commands. SecurityCenter. Models. SqlInformationProtectionPolicy. PSSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="9e4e7-120">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="9e4e7-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9e4e7-121">NOTES</span></span>

## <span data-ttu-id="9e4e7-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9e4e7-122">RELATED LINKS</span></span>
