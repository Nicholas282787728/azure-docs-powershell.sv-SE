---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: bd9b47b54cb609a06da10488007f55d91d157b90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582236"
---
# <span data-ttu-id="0fd3b-101">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="0fd3b-101">Get-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="0fd3b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0fd3b-102">SYNOPSIS</span></span>
<span data-ttu-id="0fd3b-103">Hämtar en lista över återställnings tjänstens valv.</span><span class="sxs-lookup"><span data-stu-id="0fd3b-103">Gets a list of Recovery Services vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0fd3b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0fd3b-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0fd3b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0fd3b-105">DESCRIPTION</span></span>
<span data-ttu-id="0fd3b-106">Cmdleten **Get-AzureRmRecoveryServicesVault** hämtar en lista över återställnings tjänst valv i den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="0fd3b-106">The **Get-AzureRmRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="0fd3b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0fd3b-107">EXAMPLES</span></span>

## <span data-ttu-id="0fd3b-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0fd3b-108">PARAMETERS</span></span>

### <span data-ttu-id="0fd3b-109">-Namn</span><span class="sxs-lookup"><span data-stu-id="0fd3b-109">-Name</span></span>
<span data-ttu-id="0fd3b-110">Anger namnet på valvet du vill fråga efter.</span><span class="sxs-lookup"><span data-stu-id="0fd3b-110">Specifies the name of the vault to query for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fd3b-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fd3b-111">-ResourceGroupName</span></span>
<span data-ttu-id="0fd3b-112">Anger namnet på den Azure-adressresurs som du vill skapa eller från vilken det angivna Recovery Services-objektet ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="0fd3b-112">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fd3b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fd3b-113">-DefaultProfile</span></span>
<span data-ttu-id="0fd3b-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0fd3b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0fd3b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fd3b-115">CommonParameters</span></span>
<span data-ttu-id="0fd3b-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fd3b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fd3b-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fd3b-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fd3b-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0fd3b-118">INPUTS</span></span>

## <span data-ttu-id="0fd3b-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0fd3b-119">OUTPUTS</span></span>

### <span data-ttu-id="0fd3b-120">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. RecoveryServices. ARSVault]</span><span class="sxs-lookup"><span data-stu-id="0fd3b-120">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.RecoveryServices.ARSVault]</span></span>

## <span data-ttu-id="0fd3b-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0fd3b-121">NOTES</span></span>

## <span data-ttu-id="0fd3b-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0fd3b-122">RELATED LINKS</span></span>

[<span data-ttu-id="0fd3b-123">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="0fd3b-123">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="0fd3b-124">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="0fd3b-124">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="0fd3b-125">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="0fd3b-125">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


