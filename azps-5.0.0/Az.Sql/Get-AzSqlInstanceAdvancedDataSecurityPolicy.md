---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceadvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 8adb699375a1b53f20e6027f35772642c658928b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322335"
---
# <span data-ttu-id="53a85-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="53a85-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="53a85-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="53a85-102">SYNOPSIS</span></span>
<span data-ttu-id="53a85-103">Hämtar avancerad data säkerhets princip för en hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="53a85-103">Gets Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="53a85-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="53a85-104">SYNTAX</span></span>

```
Get-AzSqlInstanceAdvancedDataSecurityPolicy [-InputObject <AzureSqlManagedInstanceModel>]
 -InstanceName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="53a85-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="53a85-105">DESCRIPTION</span></span>
<span data-ttu-id="53a85-106">Cmdleten **Get-AzSqlInstanceAdvancedDataSecurityPolicy** hämtar den avancerade data säkerhets policyn för en hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="53a85-106">The **Get-AzSqlInstanceAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="53a85-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="53a85-107">EXAMPLES</span></span>

### <span data-ttu-id="53a85-108">Exempel 1: hämtar den hanterade instansens avancerade data säkerhet</span><span class="sxs-lookup"><span data-stu-id="53a85-108">Example 1: Gets managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Get-AzSqlInstanceAdvancedDataSecurityPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" `

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="53a85-109">Exempel 2: hämtar en avancerad data säkerhet för hanterade instanser från den hanterade instans resursen</span><span class="sxs-lookup"><span data-stu-id="53a85-109">Example 2: Gets managed instance Advanced Data Security from managed instance resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Get-AzSqlInstanceAdvancedDataSecurityPolicy

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

## <span data-ttu-id="53a85-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="53a85-110">PARAMETERS</span></span>

### <span data-ttu-id="53a85-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53a85-111">-DefaultProfile</span></span>
<span data-ttu-id="53a85-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="53a85-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53a85-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="53a85-113">-InputObject</span></span>
<span data-ttu-id="53a85-114">Det hanterade instans objekt som ska användas med den avancerade åtgärden för data säkerhets princip</span><span class="sxs-lookup"><span data-stu-id="53a85-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53a85-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="53a85-115">-InstanceName</span></span>
<span data-ttu-id="53a85-116">SQL-databas hanterat instans namn.</span><span class="sxs-lookup"><span data-stu-id="53a85-116">SQL Database managed instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53a85-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53a85-117">-ResourceGroupName</span></span>
<span data-ttu-id="53a85-118">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="53a85-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="53a85-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53a85-119">CommonParameters</span></span>
<span data-ttu-id="53a85-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53a85-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53a85-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="53a85-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53a85-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="53a85-122">INPUTS</span></span>

### <span data-ttu-id="53a85-123">Microsoft. Azure. commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="53a85-123">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="53a85-124">System. String</span><span class="sxs-lookup"><span data-stu-id="53a85-124">System.String</span></span>

## <span data-ttu-id="53a85-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="53a85-125">OUTPUTS</span></span>

### <span data-ttu-id="53a85-126">Microsoft. Azure. commands. SQL. AdvancedThreatProtection. Model. ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="53a85-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="53a85-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="53a85-127">NOTES</span></span>

## <span data-ttu-id="53a85-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="53a85-128">RELATED LINKS</span></span>
