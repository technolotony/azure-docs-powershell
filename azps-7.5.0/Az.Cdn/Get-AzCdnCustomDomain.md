---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 53246003-D1E9-4863-94E9-8E0BF1272134
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/main/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/main/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
---

# Get-AzCdnCustomDomain

## SYNOPSIS
Gets a CDN custom domain.

> [!NOTE]
>This is the previous version of our documentation. Please consult [the most recent version](/powershell/module/az.cdn/get-azcdncustomdomain) for up-to-date information.

## SYNTAX

### ByFieldsParameterSet (Default)
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByObjectParameterSet
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzCdnCustomDomain** cmdlet gets an Azure Content Delivery Network (CDN) custom domain and its related settings.

## EXAMPLES

### Example 1
```powershell
Get-AzCdnCustomDomain -ResourceGroupName myresourcegroup -ProfileName mycdnprofile -EndpointName myendpoint
```

```Output
HostName                        : cdn.example.com
ValidationData                  :
ResourceState                   : Active
CustomHttpsProvisioningState    : Disabled
CustomHttpsProvisioningSubstate : None
ResourceGroupName               : myresourcegroup
ProfileName                     : mycdnprofile
EndpointName                    : myendpoint
Id                              : /subscriptions/11111111-1111-1111-1111-111111111111/resourcegroups/myresourcegroup/providers
                                  /Microsoft.Cdn/profiles/mycdnprofile/endpoints/myendpoint/customdomains/cdn-example-com
Name                            : cdn-example-com
Type                            : Microsoft.Cdn/profiles/endpoints/customdomains
ProvisioningState               : Succeeded
```

## PARAMETERS

### -CdnEndpoint
Specifies the CDN endpoint object of which the custom domain is a member.

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -CustomDomainName
Specifies the name of the custom domain.
The name of the custom domain differs from the host name of the custom domain.

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

### -DefaultProfile
The credentials, account, tenant, and subscription used for communication with azure

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

### -EndpointName
Specifies the name of the endpoint to which the custom domain belongs.

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProfileName
Specifies the name of the Profile to which the custom domain belongs.

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Specifies the name of the resource group to which the custom domain belongs.

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint

## OUTPUTS

### Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain

## NOTES

## RELATED LINKS

[New-AzCdnCustomDomain](./New-AzCdnCustomDomain.md)

[Remove-AzCdnCustomDomain](./Remove-AzCdnCustomDomain.md)


