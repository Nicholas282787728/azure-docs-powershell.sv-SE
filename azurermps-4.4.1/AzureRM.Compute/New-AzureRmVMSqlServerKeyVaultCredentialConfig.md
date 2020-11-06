---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
Module Name: Azure
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: 922c7e7055c51990b28b472805a68563c94b3e6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585740"
---
# <span data-ttu-id="a8663-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="a8663-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="a8663-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a8663-102">SYNOPSIS</span></span>
<span data-ttu-id="a8663-103">Skapar ett konfigurations objekt för SQL Server Key valv-autentiseringsuppgifter på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="a8663-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8663-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a8663-104">SYNTAX</span></span>

```
New-AzureVMSqlServerKeyVaultCredentialConfig [-Enable] [[-CredentialName] <String>]
 [[-AzureKeyVaultUrl] <String>] [[-ServicePrincipalName] <String>] [[-ServicePrincipalSecret] <SecureString>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="a8663-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a8663-105">DESCRIPTION</span></span>

## <span data-ttu-id="a8663-106">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a8663-106">EXAMPLES</span></span>

## <span data-ttu-id="a8663-107">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a8663-107">PARAMETERS</span></span>

### <span data-ttu-id="a8663-108">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="a8663-108">-Enable</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8663-109">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="a8663-109">-CredentialName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8663-110">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="a8663-110">-AzureKeyVaultUrl</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8663-111">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="a8663-111">-ServicePrincipalName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8663-112">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="a8663-112">-ServicePrincipalSecret</span></span>
```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8663-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="a8663-113">-Profile</span></span>
<span data-ttu-id="a8663-114">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="a8663-114">@{Text=}</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Utilities.Common.AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8663-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a8663-115">-InformationAction</span></span>
<span data-ttu-id="a8663-116">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="a8663-116">@{Text=}</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8663-117">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a8663-117">-InformationVariable</span></span>
<span data-ttu-id="a8663-118">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="a8663-118">@{Text=}</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8663-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8663-119">CommonParameters</span></span>
<span data-ttu-id="a8663-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8663-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8663-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8663-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8663-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a8663-122">INPUTS</span></span>

## <span data-ttu-id="a8663-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a8663-123">OUTPUTS</span></span>

## <span data-ttu-id="a8663-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a8663-124">NOTES</span></span>

## <span data-ttu-id="a8663-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a8663-125">RELATED LINKS</span></span>

